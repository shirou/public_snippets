---
title: json logging by using python-json-logger
tags:
  - python
---
import datetime
import logging
import sys

from pythonjsonlogger import jsonlogger


def get_logger(name):
    handler = logging.StreamHandler(stream=sys.stdout)
    formatter = CustomJsonFormatter("%(time)s %(level)s %(message)s")
    handler.setFormatter(formatter)
    logger = logging.getLogger(name)
    logger.addHandler(handler)
    logger.setLevel(logging.INFO)
    logger.propagate = False
    return logger


class CustomJsonFormatter(jsonlogger.JsonFormatter):
    def add_fields(self, log_record, record, message_dict):
        super(CustomJsonFormatter, self).add_fields(log_record, record, message_dict)
        if not log_record.get("time"):
            now = datetime.datetime.utcnow().strftime("%Y-%m-%dT%H:%M:%S.%fZ")
            log_record["time"] = now
        if log_record.get("level"):
            log_record["level"] = log_record["level"].upper()
        else:
            log_record["level"] = record.levelname


logger = get_logger(__file__)


obj = {
    "success": True,
    "statistics": {
        "evaluated_expectations": 19,
        "successful_expectations": 19,
        "unsuccessful_expectations": 0,
        "success_percent": 100.0,
    },
    "results": [
        {
            "meta": {},
            "success": True,
            "exception_info": {
                "raised_exception": False,
                "exception_message": None,
                "exception_traceback": None,
            },
        }
    ],
}


logger.info("foo", extra=obj)
