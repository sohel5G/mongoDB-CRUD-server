----------------------------------
MongoDB Connection 
----------------------------------
1. Creat account
2. Create an user with password
3. Network access > add IP address > Whitelist IP address
4. Database > connect > Driver > Node View Full code
5. Chnage the password in the URI


----------------------------------
CREATE (Server Side)
----------------------------------
1. App.post('/users' async (req, res) = {})
2. Make the function async to use await inside it
3. Make sure you used express.json() middleware
4. Access data from the body (const use = req.body)
5. const result = await userCollection.insertOne(user)
6. res.send(result)


----------------------------------
CREATE (Client Side)
----------------------------------
1. Create fetch 
2. add second parameter as and object 
3. provide method: 'POST'
4. add headers: {'Content-Type': 'application/json'}
5. add body: JSON,Stringify(user)



----------------------------------
READ MANY (Server Side)
----------------------------------
1. Create a curson = userCollection.find()
2. const result = await cursor.toArray()
3. res.send(result)



----------------------------------
READ MANY (Client Side)
----------------------------------
1. Create fetch OR use loader in the router 



----------------------------------
DELETE (Server Side)
----------------------------------
1. create app.delete('/user/:id', (req, res) => {})
2. Specify unique ObjectId to delete the right user (const id = req.params.id;)
3. const query = {_id:new ObjectId(id)}
4. const result = await userCollection.deleteOne(query);



----------------------------------
DELETE (Client Side)
----------------------------------
1. (fetch(`http://localhost:3000/users/${_id}`)
2. add second parameter as and object 
3. provide method: 'DELETE'









