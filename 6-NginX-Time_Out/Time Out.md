# What are timeouts?

Timeouts set a max wait time on a request. We can think about timeouts in two contexts: the client and the server. <br> Client timeouts set a limit on how long they are willing to wait for a response to come back—and in some cases be completed.<br> Server timeouts set a limit on how long the connection should remain open. For example, if a client is taking an exceptionally long time to receive a response, the server may choose to close the connection. <br>
Be careful not to limit your thinking of client as browser and server as backend. The client is the application making the request.

# Choosing a timeout value

Determining your ideal timeout involves many variables. Connection timeouts should be kept short, while read and write timeouts are more dependant on the needs of the service. There are some considerations to make when determining the ideal timeout duration for each API call.


# So what should you do?

Ideally, set specific timeouts for each API call your application makes. Use the needs of the interaction, or your services, to determine what the maximum timeout should be. <br> If you're using an HTTP library or module that doesn't surface an easy configuration for this, consider switching to one that does.

Setting custom timeouts for every request can be tedious, especially when you don't have the data necessary to make an informed decision. <br>
For example, you can set all third-party APIs that you know are further away to a higher timeout than those with local servers. This allows you to manage these limits separate from your codebase, which makes experimentation easier. It also makes adapting to unexpected network conditions easier.


