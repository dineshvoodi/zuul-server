- This is an example of Zuul server
- Applications used in this example are zuul-proxy, feign-client
- Test the application using http://localhost:9008/feign/callStatus . Request will be feign-client service.
    Since in the properties we provided ${zuul.routes.feign-client.path} as '/feign/**'. 
    So any request coming with feign text will be detected and routed to url provided in ${zuul.routes.feign-client.url}
- In this example request URL is  http://localhost:9008/feign/callStatus. Here URL contains 'feign/**', this URL is routed to feign-client service.
  The URI path after text 'feign' in the URL (i.e. callStatus) will be appended to route URL (i.e. http://localhost:9007/) which will become http://localhost:9007/callStatus