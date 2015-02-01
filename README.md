# Framework-for-HTML5-indexedDB
It provides methods allowing simple querying and manipulation of HTML5's IndexedDB to have MongoDB like queries

## Create A Datastore
indexed('sampleDB').create(); 

## Insert Records
indexed('sampleDB').insert({  
    name: 'Deepanshu Singh'
    email: 'tweetlikeme@gmail.com'
}, function (err, data) {
    if (err) {
        console.log('Error');
    } else {
        console.log(data);
    }
});

## Find Records
indexed('sampleDB').find({_id: 458799},function (err, data) {  
    if (err) {
        console.log('Error');
    } else {
        console.log(data);
    }
});

## Update Records
indexed('sampleDB').update({  
    _id: 458799
}, {
    name: 'Elon'
}, function (err, data) {
    // Handle response...
});

## Deleting Records
indexed('sampleDB').delete({  
    _id: 458799
}, function (err, data) {
    // Handle response...
});
