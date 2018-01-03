# Project Title
es-extract

## Description
 This node module make simple the data transfer from one index to another index for specific type. It is based on elasticsearch scan and scroll api and _bulk api. 
 The scan search type and the scroll API are used together to retrieve large numbers of documents from Elasticsearch efficiently, without paying the penalty of deep pagination.
 We can customize the scroll size based on the computation power of the elasticsearch server.The bulk API makes it possible to perform many  operations in a single API call. 
 This can greatly increase the indexing speed. Inthis case we are using bulk create operation.

## Prerequisite
We need to take care about mapping of the type. Mapping must be same for the type at source index and destination index, otherwise data loss issue might be happened.

### Getting Started
```
npm i es-extract --save

sample code:

var extract = require('es-extract');

var config = {
        "scroll_length":500,
        "index":"source_index",
        "destination_index":"test_001",
        "source_server": "source_server_url" ,
        "type": "test_type",
        "destination_server": "destination_server_url"
    };

    try{
        extract(config)
    }
    
    catch(e){

        console.log(e)
    }
```


## Authors

* **Barnendu Pal** - *Initial work* 



## License

This project is licensed under the MIT License.




"# es-extract" 
