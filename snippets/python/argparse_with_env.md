---
description: parse flags with environment variables
tags:
  - python
---
import argparse
import os

def parse_flag():
    parser = argparse.ArgumentParser(description="something")

    parser.add_argument(
        "--end-date",
        type=str,
        default=os.environ.get("END_DATE", None),
        help="end data (YYYY-MM-DD)",
    )

    args = parser.parse_args()
    if not args.config:
        parser.print_usage()
        sys.exit(1)

    return args
