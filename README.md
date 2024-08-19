# XTC-Authentication
This is a C# wrapper for a simple C++ library I made for unity mods that need an authentication system that doesn't lag.

## How it works
The C++ library is used as an embedded resource in your C# assembly, the wrapper is put into the project, then do whatever.
Once you put the wrapper in the project you can make an start and an update void to authenticate the key then regenerate the session every like 60 seconds.
Sessions expire every 5 minutes so make sure your refreshing it before it expires.
There should be no fps drop when using it.

## C++ Library Exports
AuthWithLicense (authenticates and opens a session ticket) - Params: string (License), string (Publishable key you get in the dashboard coming soon) <br>
RegenSession (Calls the session api and resets your session) - Params: string (SessionID you get this from the wrapper's json output), string (License), string (Publishable key) <br>
CallPortal (webhook stuffs) - Params: string (messageToPortal), string (Publishable key) <br>
more soon
