# Player DNA

Detect player identities across accounts.

## Sources of identifiers
- player information: like language, IP address (hashed of course)
- The way the player types
- Way they chat in-game
- The similarity of the username
- Items they keep on their hotbar
- Time of Play: Analyse the time when players are most active. Do certain accounts consistently play at the same time?
- If two players are online and are both moving/doing something at the same time, then this decreases their similarity score.

# Data Privacy commitment
Players can opt out of fingerprinting with `/toggle_fingerprinting`.

IP addresses and other unique identifiers are hashed with `minetest.get_password_hash(server_wide_salt, identifier)`

# Useful methods
`minetest.get_player_information(name)` - Various unique info about the player
`minetest.get_objects_inside_radius(pos, radius)` - Look at frequently visited areas
`minetest.get_objects_in_area(pos1, pos2)` - Look at frequently visited areas
`minetest.get_player_window_information(player_name)` - Fingerprint screen
