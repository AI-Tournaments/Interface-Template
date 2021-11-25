# AI-Tournaments interface template
**Quick notes**
- `window.opener.postMessage(null, '*')` at [line 20](https://github.com/AI-Tournaments/Interface-Template/blob/main/index.html#L20) signals that all dependencies has been loaded and that the interface is ready for work.
- `_init` will be an object with objects for `settings` and `opponents`, same as for [participant init](https://github.com/AI-Tournaments/Participant-Template/blob/main/participant.js#L4).
- Call `window.opener.postMessage(/*Replace with your response*/, '*')` whenever after reception of a `messageEvent.data.type === 'Post'`. You can only respond once per `Post`, other responses in between will be dropped.
- The main difference between an interface and `participant.js` is that interfaces is not sandboxed (limited or restricted) like participants. The main use case for interfaces is to debug or train participants, but interfaces can be used as an human interface to allow unranked human vs machine or human vs human matches.
- Add topic `AI-Tournaments-Interface` to make it discoverable.
