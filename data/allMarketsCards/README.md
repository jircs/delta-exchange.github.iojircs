# All Markets Card Area Config

- Order of the cards is defined by their position within this file. 
- Currently there are two files for Devnet ( devnet.json ) and Production ( prod.json ) 
- Always make changes on devnet first and verify those are working fine, then only paste same changes on production.
- After editing the file always copy the entire contents of the file and paste [here](https://jsonformatter.org/ "here") then click on Validate. A popup should show up on top right stating "Valid JSON". If it shows any error then the JSON structure is not correct.

--------------------

## Supported Custom Cards Type
-  "type" : "tradeFarming"
- "type": "offerTimeline"
- "type" : "topOptions"


---------------

## Desktop Cards

| Property  | Description  | Data Type |Example | Available for Custom / Image Card| Required / Optional Field |
|--|--| -- |-- | -- | -- |
| type |  A unique identifier for the card. This field should be unique among all the cards. Incase you need some custom card's type value please contact the developer. | string | "type": "topOptions"  | Both | Required |
| analyticsTag | Card Name which should be reported to Mixpanel and Google Analytics. On Card click events will be dispatched with this value. | string| "analyticsTag": "Staking_Pool"  | Both | Required |
| imageURL | Link for the image which needs to be shown  | string | "imageURL": "SOME_URL"  | Only Image Card | Required |
| redirectURL | Link where user should be redirect on card click. | string | "redirectURL": "SOME_URL"  | Only Image Card | Required |
| openInNewTab | When card is clicked should that be opened in new tab or same tab. If the provided value is true then open in new tab else if false then open in same tab | true or false | "openInNewTab" : true | Only Image Card | Required |
| showWhenLogin | Show the card only when user is logged in or logged out state or both. If not specified then card is shown in all the states. | "preLogin" or "postLogin" | "showWhenLogin" : "preLogin" | Both | Optional |



## Mobile Cards

| Property  | Description  | Data Type |Example | Available for Custom / Image Card| Required / Optional Field |
|--|--| -- |-- | -- | -- |
| type |  A unique identifier for the card. This field should be unique among all the cards. Incase you need some custom card's type value please contact the developer. | string | "type": "topOptions"  | Both | Required |
| analyticsTag | Card Name which should be reported to Mixpanel and Google Analytics. On Card click events will be dispatched with this value. | string| "analyticsTag": "Staking_Pool"  | Both | Required |
| imageURL | Link for the image which needs to be shown  | string | "imageURL": "SOME_URL"  | Only Image Card | Required |
| redirectURL | Link where user should be redirect on card click. | string | "redirectURL": "SOME_URL"  | Only Image Card | Required |
| openInNewTab | When card is clicked should that be opened in new tab or same tab. If the provided value is true then open in new tab else if false then open in same tab. NOTE- For Mobile App this option won't work. Irrespective of the value it will always open in same tab as if choose to target new tab then it open's the tab outside the app within a browser which is not expected behavior.  | true or false | "openInNewTab" : true | Only Image Card | Required |
| showWhenLogin | Show the card only when user is logged in or logged out state or both. If not specified then card is shown in all the states. | "preLogin" or "postLogin" | "showWhenLogin" : "preLogin" | Both | Optional |
| showWhenMobile | Show the card only when user is in mobile browser or mobile app or both. If not specified then card is shown in all the states | "browser" or "app" | "showWhenMobile" : "app" | Only Image Card | Optional |
