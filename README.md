This repo is for practice only. just ignore this repo unless you wanna look at the codes

# Some method
- post -> post.save()       // save datas to local then use res.json() to upload on server
- get -> post.findById()   // select specific data with params
- patch -> post.updateOne()  // change data with {_id:req.params.Id}, {$set:{title:req.body.title ,etc.}}
- delete -> post.remove()     //delete data with {_id:req.params.Id}



# Deploy node.js application on AWS with github [tutorial](https://sumantmishra.medium.com/how-to-deploy-node-js-app-on-aws-with-github-db99758294f1)

# Post and Get data from REST API with javascript [Using fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
## [handle data Tutorial](https://www.youtube.com/watch?v=Kw5tC5nQMRY)
```
async function postData (url='', data={}){
    const options = {
        method: "POST",
        headers: {
            'content-type': 'application/json'
        }
        referrerPolicy: 'no-referrer',
        body: JSON.Stringify(data),
    }
    const response = await fetch(url, options);
    return response.json();                     // parses JSON response into native JavaScript objects
 }
 postData('https://www.jaysss.site/forum/',{ title: 'new post', description: 'some random text here'})
    .then(data=>{
        console.log('success',data)
    }
```

# some initial settings

- npm install mongoose
- npm install dotenv       // require('dotenv').config();
- app.use(express.json());            // same as body-parser
router.get('/:postId', (req,res) =>{
    console.log(req.params.postId);
})
'/:postId' => https://google.com/posts/This is where shows postId;
```
