# IRC commands

/join #channel - joins a channel
/join #channelname password - joins a channel with a password
/part #channel - leaves a channel
/nick nickname - lets the user change their nickname
/quit - leaves the server
/mode +i or /mode -i makes the user visible/invisible on the list
/ignore nickname
/unignore nickname
/query the username as `/query username` in the chat message line
/msg username message works too without having to open a new window
/nick NewNickname Leaving for lunch! changes the user message
/msg #channel message sends a message to everyone in the channel
/whois nickname
/server serveraddress
/me action
/notice nickname message
/highlight text

for channel operators:
replace #channel with the channel you want to set the option

/mode #channel +v nickname grants operator privledges to a user
/mode #channel +b nickname bans a user from the channel
/mode #channel +k password sets a password for the channel
/mode #channel +m sets channel to moderated mode
/mode #channel +s sets channel to secret mode
/mode #channel -s sets channel to public mode
/mode #channel +t limits channel topic to channel operators
/mode #channel +b *.*.*.xxx bans a user by their IP address
/mode #channel +b nickname!username@hostname+#invite ban a user with an invite exception
/mode #channel +r requires a user to be registered
/mode #channel +k required_keyword requires a user to have a keyboard to join
/mode #channel +i enables channel invites
/mode #channel +N allows channel operators to sent notices
/mode #channel +b nickname* bans all users that start with a specific spring
/mode #channel +b *@example.com bans a user from a domain
/mode #channel +M protects the channel modes from being changed
/mode #channel +t <seconds> sets a message delay in seconds to prevent spam, etc
/mode #channel +o nickname grants operator privledges

/mode +R marks user as registered
/mode +w subscribes to wallops
/mode #channel +L
/mode +away message
/mode +realname Your Real Name

/kick nickname
/ban nickname
/topic #channel new topic
/away message
/version
/help [command]
/dcc send nickname filename
/dcc get nickname filename
