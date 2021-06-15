Updates existing object in the object store with given changes

Syntax
table.update(key, changes)
Parameters
key	Primary key
changes	Object containing the key paths to each property you want to change.
Return Value
Promise with the number of updated records (1 if an object was updated, otherwise 0). The reason for a result of 0 can be either that the provided key was not found, or if the provided data was identical to existing data so that nothing was updated.

Remarks
Similar to SQL UPDATE. The difference between update() and put() is that update() will only apply given changes to the object while put() will replace the entire object. Another difference is that in case key is not found, put() would create a new object while update() wont change anything. The returned Promise will NOT fail if key was not found but resolve with value 0 instead of 1.

Equivalent to Table.where(":id").equals(key).modify(changes);

Sample
db.friends.update(2, {name: "Number 2"}).then(function (updated) {
  if (updated)
    console.log ("Friend number 2 was renamed to Number 2");
  else
    console.log ("Nothing was updated - there were no friend with primary key: 2");
});
See Also
Collection.modify()

Table.put()
