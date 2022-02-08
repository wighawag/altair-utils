# pre-request scrips

## transform in lowercase every env variable starting with lc_

```js
const envKeys = Object.keys(altair.data.environment);
for (let envKey of envKeys) {
 if (envKey.startsWith("lc_")) {
   const currentValue = altair.data.environment[envKey];
   altair.helpers.setEnvironment(envKey, currentValue.toLowerCase());
 }
}
```
