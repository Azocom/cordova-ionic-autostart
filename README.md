#### INSTALL

npm i https://github.com/Azocom/cordova-ionic-autostart.git --legacy-peer-deps

npm i @ionic-native/autostart --legacy-peer-deps

# USE

import { Autostart } from '@ionic-native/autostart/ngx';

constructor(
private autostart: Autostart
) {

}

async ngOnInit() {

    this.platform.ready().then(async () => {
      this.autostart.enable();
    });

}
