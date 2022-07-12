---
description: parse flags with environment variables
tags:
  - python
---
import argparse
import os

def parse_flag() -> argparse.Namespace:
    parser = argparse.ArgumentParser(description="something")

    parser.add_argument(
        "--enddate",
        type=str,
        default=os.environ.get("ENDDATE", None),
        help="end date (YYYY-MM-DD)",
    )

    args = parser.parse_args()
    if not args.enddate:
        parser.print_usage()
        sys.exit(1)

    return args
