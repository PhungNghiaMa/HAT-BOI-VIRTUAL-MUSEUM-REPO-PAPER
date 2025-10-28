# HAT BOI VIRTUAL MUSEUM RUNNING GUIDANCE

## ***Step 1:***  
Open .env in folder ```PAPER-SUMISSION-REPO/backend``` and ```PAPER-SUBMISSION-REPO``` to import all the required data to the required field 

 ## ***Step 2:***  
### ***To test the Frontend only:***
* Run this command : 
```
  npm run dev
```
### ***To test FE + BE:*** 
* Navigate to ***```src/game_logic/index.js```*** , uncomment this line :
```javascript
  const [gltf, items] = await Promise.all([loadModelPromise , getAssetsPromise]); //[ LINE 917 ] 

  AssetDataMap.clear()  //[ LINE 921 - 927 ]
  for (const item of items){
     AssetDataMap.set(item.asset_mesh_name , item)
  }
```
* And comment this line:
```javascript
        const [gltf] = await Promise.all([loadModelPromise]); // [ LINE 918 ]

```
* Run this command to start both FE + BE:
```
  npm run all
```

