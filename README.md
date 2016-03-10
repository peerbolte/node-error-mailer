node-error-mailer
=================

A small, simple module that allows you to send errors to an e-mail address using smpt

## Installation

    npm install node-error-mailer
    
## Usage

    var nodeErrorMailer = require ('./index.js');

    var options = {
        fromEmail: 'from.user@yourdomain.com',
        toEmail: 'from.user@yourdomain.com',
        appName: 'Test App',
        smpt: {
            host: 'smtp.yourdomain.nu',
            port: 587,
            auth: {
                user: 'user@yourdomain.nu',
                pass: 'password'
            }
        }
    }

    nodeErrorMailer.init(options);

    nodeErrorMailer.send('an error occured', function(err, data){
        console.log(err, data);
    });


## TODO 

- Add throttle to max errors per time period

## Release History

* 0.0.1 Initial Working Version