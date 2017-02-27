# SQLcap

A modified version of Hood3dRob1n's PHP front-end SQLmap GUI interfacing with SQLmap's JSON API.

Credit first to SQLmap developers [Bernardo Damele](bernardo@sqlmap.org) ([@insuisb](https://twitter.com/inquisb)) and [Miroslav Stampar](miroslav@sqlmap.org) ([@stamparm](https://twitter.com/stamparm)). The SQLmap project is licensed under the [GNU General Public License v2.0](http://www.gnu.org/licenses/gpl-2.0.html).

Credit also belongs to [Hood3dRob1n](https://github.com/Hood3dRob1n) who provided the foundations for this project. Their project is not licensed at this time.

The following usage disclaimer is inherited from the sqlmap project:

> Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program.

# Usage

Use the following steps to set up the service:

 1. Navigate to the directory `/var/www/html/` or `/var/www/` if the `html` directory doesn't exist (Linux only).
 2. Clone this repository: `sudo git clone https://github.com/tjgerot/SQLcap`.
 3. Ensure Apache, Python, SQLmap, and PHP are all installed.
 4. In a new terminal tab/window run `python sqlmapapi.py -s` to start the SQLmap API server.
 5. If Apache isn't running, start it with the command `sudo service apache2 start`.

Use the following steps to access and the GUI:

### Local Access

Open a browser on the machine and navigate to `http://localhost/SQLcap`

### Remote Access

If on the same private network as the Linux device running the PHP server, navigate to the IP of the server which can be found through `ifconfig` on server (e.g. `192.168.0.102/SQLcap`).

If accessing from outside the server's private network, naviate to the forwarded IP and port of the server's apache service (e.g. `http://174.76.54.32/SQLcap`).
