## GFW settings
- Don't modify `user-rule` in the interface unless you want to set it back to **default**

### Step 1: open `gfwlist.js`
```sh
nano ~/.ShadowsocksX-NG/gfwlist.js
```
### Step 2: copy and paste the `gfwlist.js` content
#### If you are stay overseas
```javascript
// some code
for (var i = 0; i < rules.length; i++) {
  defaultMatcher.add(Filter.fromText(rules[i]));
}
// some code
```
#### If you are in China
```javascript
// some code
for (var i = 0; i < inwardsRules.length; i++) {
  defaultMatcher.add(Filter.fromText(inwardsRules[i]));
}
// some code
```
### Step 3: Reboot shadowsocks