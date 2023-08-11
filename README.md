# Smart-Mirror

AI-based Smart Multipurpose Digital Mirror

The mirror looks like a normal mirror but as soon as we start operating it it turns into a full-fledged digital screen with built-in Google Assistant to support it via audio commands also. The mirror provides a functional, user-friendly and interactive UI to its user for accessing their social sites, messengers, etc... The intention of making it is to integrate all these technologies to implement a low-cost, easy-to-use wireless domotic system along with a real-time monitoring system to improve the Quality of Life.

Steps for Installing the Software:
   
   LINUX
   Download and install the latest Node.js version:

    curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -
    sudo apt install -y nodejs

    Clone the repository and check out the master branch: git clone https://github.com/MichMich/MagicMirror
    Enter the repository: cd MagicMirror/
    Install the application: npm run install-mm
    Make a copy of the config sample file: cp config/config.js.sample config/config.js
    Start the application: npm run start

   WINDOWS
   Install dependencies in the vendor and font directories:

Powershell:

    cd fonts; npm install; cd ..
    cd vendor; npm install; cd ..

Command Prompt:

    cd fonts && npm install && cd ..
    cd vendor && npm install && cd ..

Otherwise, the screen will stay black when starting the MagicMirror.

Fix the start script in the package.json file:

    Navigate to the file package.json
    Find where it says

    "start": "DISPLAY=\"${DISPLAY:=:0}\" ./node_modules/.bin/electron js/electron.js",
    "start:dev": "DISPLAY=\"${DISPLAY:=:0}\" ./node_modules/.bin/electron js/electron.js dev",

    and replace it with

    "start": ".\\node_modules\\.bin\\electron js\\electron.js",
    "start:dev": ".\\node_modules\\.bin\\electron js\\electron.js dev",

Otherwise, the program won't start, but will display this error message: "'DISPLAY' is not recognized as an internal or external command, operable program or batch file."

For Further Details visit, https://docs.magicmirror.builders 
 
