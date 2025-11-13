The user has gathered a new viewpoint(s) in the my-hot-takes queue folder:

my-hot-takes/processed

You should do the following:

1) Identify the hot take increment from log.json and rename the hot take file with the next incremental value. If the last hot take was 001 then you should rename this file 002_hottake.md

2)  Delegate the rebuttal formulation to the hot take responder subagent. 
 
When the subagent has formulated their response you save it to: claude-responses using this filename 002_response.md where 002 is the corresponding number.

THEN:

Update log.json with a JSON object providing: relative path to hot take (from repo base), relative path to response (from repo base)

If the JSON file is empty, start the array. 

FINALLY:

Ask the user if they'd like you to send them the debate. You can use an MCP to send it to them by email or save it to a wiki. 