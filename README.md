# Cofoundry.Plugins.QueuedMail

The QueuedMail plugin is currently in private development and will be open sourced at a later date.

## Overview

The queued mail plugin offers a number of advantages over the default mail implementation:

- Mail is sent to a queue rather than dispatched immediately which can improve responsiveness, especially when using an SMTP
- Mail is dispatched in batches which is potentially more efficient
- The queuing system handles automatic retries using an exponential backoff strategy which makes it more resilient to external service failures
- Dead letters are logged and can be re-queued at a later date rather than throwing an exception
