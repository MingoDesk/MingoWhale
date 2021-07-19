# How to update users perms

**Staff admin**

```shell
db.Users.findOneAndUpdate({ _id: "github|16852656"}, { $set: { permissions: [ "edit:notes", "edit:other-user-settings", "edit:system-settings", "edit:all-tickets", "view:all-tickets", "view:all-organisation-tickets", "create:note", "reply:ticket", "create:ticket", "view:ticket" ] }}, { returnOriginal: false });
```
