iPhone Remote
=============

mru <mru@sisyphus.teil.cc>


A simple web application that allows executing functions on the server
via a webinterface on the iPhone.

![Screenshot](https://github.com/mru00/iphone-remote/blob/master/screenshot-1.png?raw=true "Screenshot")


Adding Command
--------------

Add commands to the 'Commands' class decorated as staticmethod.


    class Commands:

        @staticmethod
        def standby():
            """Standby"""
            pass


Then, add them to the HTML page. You can refer to a command with the
'${link("func-name")}' call in the 'content' string.

    <h2>Audio</h2>

     <table>
      <tr>
       ${link("vol_down")}
       ${link("vol_up")}
      <tr>
       ${link("mute", colspan=2)}
     </table>


Architecture
------------

 - mako for HTML rendering
 - SimpleHTTPServer as server
