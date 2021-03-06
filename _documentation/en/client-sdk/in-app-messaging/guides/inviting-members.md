---
title: Inviting Members
navigation_weight: 2
---


# Inviting Members


## Overview

This guide covers inviting users to a conversation (members), listening for invites to join a conversation as well as new members joining.

Before you begin, make sure you [added the SDK to your app](/client-sdk/setup/add-sdk-to-your-app) and you are able to [create a conversation](/client-sdk/in-app-messaging/guides/simple-conversation).

```partial
source: _partials/client-sdk/messaging/chat-app-tutorial-note.md
```

This guide will introduce you to the following concepts.

- **Invites** - you can invite users to a conversation
- **Application Events** - `member:invited` events that fire on an Application, before you are a Member of a Conversation
- **Conversation Events** - `member:joined` and `text` events that fire on a Conversation, after you are a Member


## Listening for Conversation invites and accepting them

```tabbed_content
source: _tutorials_tabbed_content/client-sdk/guides/messaging/inviting-members/invited
```


## Listening for members who joined a conversation
```tabbed_content
source: _tutorials_tabbed_content/client-sdk/guides/messaging/inviting-members/joined
```

## Inviting users to a conversation

Users can be invited to join conversation - their username will be used:

```tabbed_content
source: _tutorials_tabbed_content/client-sdk/guides/messaging/inviting-members/invite
```

