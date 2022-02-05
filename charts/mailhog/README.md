# Mailhog

Packaged application : [![GitHub](https://img.shields.io/badge/-mailhog%2FMailHog-black?logo=github&style=flat)](https://github.com/mailhog/MailHog)

## Overview

MailHog is an email testing tool for developers:

Configure your application to use MailHog for SMTP delivery
View messages in the web UI, or retrieve them with the JSON API
Optionally release messages to real SMTP servers for delivery

## Features

See [MailHog libraries](https://github.com/mailhog/MailHog/tree/master/docs/LIBRARIES.md) for a list of MailHog client libraries.

* ESMTP server implementing RFC5321
* Support for SMTP AUTH (RFC4954) and PIPELINING (RFC2920)
* Web interface to view messages (plain text, HTML or source)
  * Supports RFC2047 encoded headers
* Real-time updates using EventSource
* Release messages to real SMTP servers
* Chaos Monkey for failure testing
  * See [Introduction to Jim](https://github.com/mailhog/MailHog/tree/master/docs/JIM.md) for more information
* HTTP API to list, retrieve and delete messages
  * See [APIv1](https://github.com/mailhog/MailHog/tree/master/docs/APIv1.md) and [APIv2](https://github.com/mailhog/MailHog/tree/master/docs/APIv2.md) documentation for more information
* HTTP basic authentication (values.yaml => mailhog.config.http.authUser) for MailHog UI and API
* Multipart MIME support
* Download individual MIME parts
* In-memory message storage
* file based storage for message persistence
* Lightweight and portable

## Not implemented

MailHog can store messages in MongoDB, this chart doesn't support this feature for now