You can use the commands listed 

http://technet.microsoft.com/en-us/library/cc725766%28WS.10%29.aspx

here to manage Terminal Server connections. query session /server:<servername> is probably the first one you want.
These all require remote procedure call, which is part and parcel with CIFS/SMB (the IPC$ share). Check that the RPC service is enabled first. Second, you can't/shouldn't (depending on network configuration) run these services over anything but the local network. If you're trying to do this sort of management over the Internet, you should be using a VPN or some creative SSH tunneling.
