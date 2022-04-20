# How to update users perms

**Staff admin**

```shell
db.Users.findOneAndUpdate({ providerId: "110641983501304607128"}, { $set: { permissions: [ "edit:notes", "edit:other-user-settings","view:all-tickets", "view:all-organisation-tickets", "view:all-tickets", "view:all-organisation-tickets", "create:note", "reply:ticket", "create:ticket", "view:ticket" ] }}, { returnOriginal: false });
```

Create indexes for providerId:

```shell
db.User.createIndex({providerId: 1}, { unique: true });
```

edit:notes
edit:other-user-settings
view:all-tickets
view:all-organisation-tickets
create:note
reply:ticket
create:ticket
view:ticket