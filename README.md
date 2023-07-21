## INSTALL

npm i https://github.com/Azocom/cordova-ionic-autostart.git --legacy-peer-deps

npm i @ionic-native/autostart --legacy-peer-deps

#### Optional

npm i @awesome-cordova-plugins/core --legacy-peer-deps

### Using IONIC 6

1 - App.Module

import { Autostart } from '@ionic-native/autostart/ngx';

providers: [
Autostart,
......
],

---

2 - App.Component

import { Autostart } from '@ionic-native/autostart/ngx';
import { Platform } from '@ionic/angular';

export class AppComponent implements OnInit {

constructor(
private platform: Platform,
private autostart: Autostart
) {

}

async ngOnInit() {

      this.platform.ready().then(async () => {
        this.autostart.enable();
      });

}

}
