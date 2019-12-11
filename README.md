# Plugin: `roblox-profile`

This plugin adds Roblox profile links to Developer Forum user profiles.

---

## Features

- Adds a link to a user's Roblox profile on the following places:

  - Forum profile (i.e. `https://devforum.roblox.com/u/Roblox`):
  <img src=docs/roblox-profile-profile.png width=60%>

  - User cards that appear when tapping on a user's icon or name on posts:
  <img src=docs/roblox-profile-usercard.png width=60%>

- The link will be in the format of: `https://www.roblox.com/users/profile?username=Roblox`

---

## Impact

### Community

Users are easily able to discover the Roblox profile of other users, without having to copy-paste the username.

### Internal

Engineers are easily able to find the Roblox profile of a user when investigating bug reports and feature requests.

### Resources

The plugin uses information already available on the client to show the labels. There is no performance impact on the forum.

While these links do make for increased traffic from the forum to Roblox user profiles, this is to be considered a highly negligible cost.

### Maintenance

There is no manual maintenance cost.

---

## Technical Scope

The plugin uses officially supported "plugin outlets" to add labels to the front-end at specific locations. There is little risk of the labels being misplaced or breaking entirely over time through Discourse updates.

The plugin only affects the front-end of the application.

The profile link is formed using only the user's forum username, which is equivalent to their (past or present) Roblox username, due to SSO configuration.

---

## Configuration

The profile links cannot be turned off without fully uninstalling the plugin.
