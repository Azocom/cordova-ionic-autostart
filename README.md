#### INSTALL

npm i https://github.com/Azocom/cordova-ionic-autostart.git --legacy-peer-deps

npm i @ionic-native/autostart --legacy-peer-deps

# Options

npm i @awesome-cordova-plugins/core --legacy-peer-deps

# USED

1 - App.Module

import { Autostart } from '@ionic-native/autostart/ngx';

providers: [
Autostart,
......
],

---

2 - App.Component

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
