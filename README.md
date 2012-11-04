thoughtstreams-api
==================

Documentation and sample code for talking to the [ThoughtStreams](https://thoughtstreams.io/) API.

API Key
-------

To use the API, you will need an API Key. You can view your API Key by looking under [Settings > API Key](https://thoughtstreams.io/account/api-key/).

Posting to Inbox
----------------

To get things started, we've just implemented posting new content to your inbox.

You just need to POST to `https://thoughtstreams.io/api/v1/inbox/` and the body of your POST will be
turned into a card in your inbox. Basic Auth is used with your API Key as the password.

For example, on the command-line, with `curl` you could type:

    curl -u "<username>:<api-key>" -X POST --data-binary @- -H "Content-Type: text/plain" https://thoughtstreams.io/api/v1/inbox/

and type a thought, then ctrl-D and an inbox card will be created.
