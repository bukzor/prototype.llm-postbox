---
label: SENDMESSAGE
standing: user
verdict: declined
authority: 'owner, 2026-08-28; revisit condition effectively none: "I
  doubt claude-code team will ''fix'' all these aspects anytime soon.
  Even if they do, i don''t trust they won''t add other problems (for
  me)."'
why:
  - ../../experience.kb/receiving-is-ungated.md
---

# SendMessage / ListAgents as the transport

The built-in push transport, declined on the owner's three grounds,
quoted:

1. "agents often decide they want to send messages for inane reasons,
   with zero-or-negative benefit, and substantial costs"
2. "agents recieving messages often get very distracted from their
   task"
3. "there's **no way** to /rewind to before a message was
   sent/recieved short of /claude-surgery"

PUSH_ROOT_CAUSE reads all three as one choice, push-into-context;
RECEIVE_UNGATED is why no configuration rescues it. Push also
structurally excludes the editing and retraction of in-flight mail
that MUTABLE_UNTIL_READ requires.
