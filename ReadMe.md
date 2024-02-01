# Gamification for android & ios platform

this package provide rewards integration of any existing system to integrate rewards and claim.

## Installation

You can install this package using npm:

```bash
npm i gamification-react-test1 
```

## Usage

1.create new page and import Gamification & pass config.<br>

import package
```bash
import Gamification from "ionic-gamification-test";
```
initialize config
```bash
const config = {
  baseUrl: "https://thelogicalbanya.com/popupdemo/dashboard.php",
  clientID: "demo",
  key: "demo",
  userID: "100031",
  username: "TheLogicalBanya",
  keyString: "bR5z6*r$00p#Eno__odrEgeW",
  appId: 'app' /* pass div id in used index.html like  <body> <div id="app"></div>< /body> */
  utm_param1 :'' // optional parameters 
  utm_param2 :'' // optional parameters 
  utm_param3 :'' // optional parameters 
  utm_param4 :'' // optional parameters 
};
Gamification.init(config);
```

open gamification
```bash
const openApp = () => {
  Gamification.run();
}
```

close gamification
```bash
const openApp = () => {
  Gamification.close();
}
```
1.vue js
```ionic
<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <div style="padding: 10px">
        <IonButton @click="openApp" type="button" mode="md" color="primary">
          Test
        </IonButton>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup>
import {IonButton, IonContent, IonPage} from '@ionic/vue';
import Gamification from "ionic-gamification-test";

const config = {
  baseUrl: "https://thelogicalbanya.com/popupdemo/dashboard.php",
  clientID: "demo",
  key: "demo",
  userID: "100031",
  username: "TheLogicalBanya",
  keyString: "bR5z6*r$00p#Eno__odrEgeW",
  appId: 'app' /* pass div id in used index.html like  <body> <div id="app"></div>< /body> */
  utm_param1 :'' // optional parameters 
  utm_param2 :'' // optional parameters 
  utm_param3 :'' // optional parameters 
  utm_param4 :'' // optional parameters 
};
Gamification.init(config);

const openApp = () => {
  Gamification.run();
}
</script>
```

in react 
```react

import React from 'react';
import {IonButton, IonContent, IonPage} from '@ionic/react';
import Gamification from "ionic-gamification-test";

const Home: React.FC = () => {
    const config = {
        baseUrl: "https://thelogicalbanya.com/popupdemo/dashboard.php",
        clientID: "demo",
        key: "demo",
        userID: "100031",
        username: "TheLogicalBanya",
        keyString: "bR5z6*r$00p#Eno__odrEgeW",
        appId: 'root' /* pass div id in used index.html like  <body> <div id="root"></div>< /body> */
    };
    Gamification.init(config);
    const open = () => {
        Gamification.run();
    }
    return (
        <IonPage>
            <IonContent fullscreen>
                <div style={{padding: 10}}>
                    <IonButton onClick={open} color={'primary'}>Test</IonButton>
                </div>
            </IonContent>
        </IonPage>
    );
};

export default Home;

```

also you can pass another optional parameters <br>
1.utm_param1 <br>
2.utm_param2 <br>
3.utm_param3 <br>
s4.utm_param4 <br>

for example
