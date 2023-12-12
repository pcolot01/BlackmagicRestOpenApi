# BlackmagicRestOpenApi
This is an OpenApi (https://www.openapis.org/) implementation of the BlackMagic Rest protocol used on their devices. 
see the specification in https://documents.blackmagicdesign.com/DeveloperManuals/BlackmagicCameraControl.pdf

Currently, only transport and lens REST components are implemented.

In api folder, the OpenApi yaml reference is provided. 
The API try to respect REST API design pattern defined in https://www.apimatic.io/blog/2022/11/14-best-practices-to-write-openapi-for-better-api-consumption

In dist folder, the unstripped Json bundle is provided for integration or reference from third party tools.



All references in yaml are local to the current file. Usually, references are URL to allow usage in a browser or in the server.
In any case, the best is to precompile the API as a standalone JSON file.

https://openapistack.co/docs/openapi-client-axios/bundling/

npm install -g openapicmd 

npx openapi read ./api/0.1.0/BlackmagicCameraControlRestAPI.yaml --format=json --dereference --bundle > dist/0.1.0/BlackmagicCameraControlRestAPI.json

or

npx openapicmd read ./api/0.1.0/BlackmagicCameraControlRestAPI.yaml --format=json --dereference --bundle > dist/0.1.0/BlackmagicCameraControlRestAPI.json


Now the following third party tools are able to generate client and server stub, documentation, documentation, ...

- https://www.openapis.org/
- https://openapistack.co/
- https://liblab.com/
- ...
