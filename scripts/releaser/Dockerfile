# --------------------------------------------------------------------------------------------
# Copyright (c) Microsoft Corporation. All rights reserved.
# Licensed under the MIT License. See License.txt in the project root for license information.
# --------------------------------------------------------------------------------------------

FROM python:3.5.2-alpine

RUN apk upgrade --no-cache && \
    apk add --no-cache bash git openssh gcc make nano vim \
      openssl-dev libffi-dev musl-dev ca-certificates openssl && update-ca-certificates

RUN pip install --no-cache-dir --upgrade pip wheel twine requests virtualenv uritemplate.py azure-cli sh

ADD . /

CMD cat README.md; printf "\n\n** starting bash...\n\n"; bash
