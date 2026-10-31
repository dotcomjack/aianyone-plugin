# AI Anyone

AI Anyone puts a real person in the conversation. Ask to hear from a named person and they arrive as a card with
their portrait, then the assistant answers as them. Call them out loud on AI Anyone, open the characters you made
yourself, or put two people in a room to argue a question while each side holds an aim the other cannot see.

## What this plugin contains

- `skills/ai-anyone/SKILL.md`: when to use AI Anyone and how to speak as a character. It is text only and runs
  nothing.
- `.mcp.json`: one remote server, `aianyone`, at `https://mcp.aianyone.com/mcp`. Nothing is installed or run on
  your computer.

## Everything it sends, and where

Every request goes to one place, the AI Anyone server at `https://mcp.aianyone.com/mcp`, over HTTPS. A tool call
sends only what that tool needs:

- a search phrase, when you look for someone to ask;
- a character id, when you open, hear or call a character;
- a debate topic and the lines written during it, while a debate runs. The debate's working buffer is deleted when
  the debate ends, or half an hour after its last turn.

The server keeps aggregate counts of tool calls by assistant family, tool and outcome, whether you were signed in and
which kind of account you hold, the name and version your assistant software reports about itself and the first 160
characters of its user agent, and the ids of studio characters a call was about. It never keeps your IP address and
nothing that identifies you. It never receives your conversation or your files, and it knows who you are only if you
choose to sign in.

Signing in is optional and happens only when you ask for your own characters. The assistant then sees the characters
you made on AI Anyone and, only where the assistant asks for it, your email address. The connection keeps your account
id, which kind of account you hold and whether it is one of our test accounts, encrypted. You can disconnect at any
time, and deleting your AI Anyone account ends every assistant connection.

Buttons on a card open pages on `https://aianyone.com` (a call, a chat, your characters) through
`https://mcp.aianyone.com/go/`, which counts the click and adds the source to the link.

## Links

- Documentation: https://mcp.aianyone.com/docs
- Privacy: https://aianyone.com/privacy#assistant-plugins
- Terms: https://aianyone.com/terms-of-service
- Support: support@aianyone.com

## License

The files in this bundle are MIT licensed. See `LICENSE`. The AI Anyone service itself is covered by its terms.
