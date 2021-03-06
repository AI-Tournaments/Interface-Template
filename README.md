# AI-Tournaments interface template
The main difference between an interface and `participant.js` is that interfaces opens in a separate browser tab and is not sandboxed (limited or restricted) like participants. The main use case for interfaces is to debug or train participants and to get a better insight in to a running match, but interfaces can also be used to allow Human vs Participant matches and even Human vs Human.

**Quick notes**
- `window.opener.postMessage({keepOpenAfterTermination: false}, '*')` on [line 40](https://github.com/AI-Tournaments/Interface-Template/blob/main/index.html#L40) signals that all dependencies has been loaded and that the interface is ready for work. Field `keepOpenAfterTermination` sigals if the interface window should be closed automatically when the interface is terminated.
- `_init` will be an object with objects for `settings` and `opponents`, same as for [participant init](https://github.com/AI-Tournaments/Participant-Template/blob/main/participant.js#L4).
- Call `window.opener.postMessage(/*Replace with your response*/, '*')` whenever after reception of a `messageEvent.data.type === 'Post'`. The HTML object `responseLock` will help with managing that only one respond is sent per `Post`.
- Add topic `AI-Tournaments-Interface` to make it discoverable.<br><i>Optional</i>
- Activate `GitHub Pages`.
