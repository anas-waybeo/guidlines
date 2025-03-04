### 1. Customer number blocking
#### Steps
1. Open _spam_numbers_ file from number repo
2. Make sure the number is non-duplicate
3. format is +91VN;ticket-no:cs eg: _+91876543210;EB-1234;Rohan_
---
### 2. VN Activation
#### Steps
1. VN number is unique. so make sure the VN is exist on number repo via postman API call GET method.
    1.a. If number is exist ask for provide new VN.
2. Add VN to number repo vai postman API call POST method.
    2.a. format
```bash
{
    "name":"app-name", // find it from GET api request
    "number":"VN", // virtual number
    "user":"developer" // if no user available add a new user
}
```
3. Check the store exist on not in _stores_ table with provided store-code
    3.a. If store not exist create with available details. also map heirarchies.
    3.b. Create callflow via console command
        3.b.1. Update store id in console command source code
4. Add VN to _numbers_ table
---
### 3. Landing number update
#### Scenarios
1. Remove existing landing number.
2. Add new landing number.
#### Project (Rarerabbit)
- Actually there is 2 store types are available. Rarerabbit and Rarerrism. both store types welcome-ivr is different. In the time of callflow creation system will take default welcome-ivr(rarerabbit). If you are trying to update the callflow of rarrerism callflow please replace the welcome-ivr filename.
#### Steps
1. Update landing number on _stores_ table.
2. Update callflow via console command.
---

[Mumbai server](mumbai_server.md)