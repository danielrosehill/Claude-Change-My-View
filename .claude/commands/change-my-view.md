The user has gathered a new viewpoint(s) in the my-hot-takes/queued folder.

You should do the following:

1) Check log.json to identify the next incremental debate ID. If the last debate was 001, then the next should be 002.

2) Move the hot take file from my-hot-takes/queued/ to my-hot-takes/processed/ and rename it with the incremental value. For example, if the next ID is 002, rename it to 002_hottake.md

3) Delegate the rebuttal formulation to the rebuttal-writer subagent.

4) When the subagent has formulated their response, save it to claude-responses/ using this filename pattern: 002_response.md where 002 is the corresponding debate ID number.

THEN:

5) Update log.json with a JSON object providing:
   - debate ID
   - timestamp
   - relative path to hot take (from repo base): my-hot-takes/processed/00X_hottake.md
   - hot take title
   - relative path to response (from repo base): claude-responses/00X_response.md
   - status: "completed"
   - word counts for both files

If the JSON file is empty or has no debates array, start the array.

FINALLY:

Ask the user if they'd like you to send them the debate. You can use an MCP to send it to them by email or save it to a wiki. 