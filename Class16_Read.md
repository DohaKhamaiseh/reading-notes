### What are the key characteristics of serverless computing, and how does it differ from traditional server-based architectures?

**Provisioning time**: Measured in milliseconds for serverless, vs. minutes to hours for the other models.

 <br/>

* **Administrative burden**: None for serverless, compared to a continuum from light to medium to heavy for PaaS, containers and VMs respectively.

  <br/>

* **Maintenance**: Serverless architectures are managed 100% by the provider. The same is true for PaaS, but containers and VMs require significant maintenance including updating/managing operating systems, container images, connections, etc.

  <br/>

* **Scaling**: Auto-scaling—including auto-scaling to zero—is instant and inherent for serverless. The other models offer automatic but slow scaling that requires careful tuning of auto-scaling rules, and no scaling to zero.

  <br/>

* **Capacity planning**: None needed for serverless. The other models require a mix of some automatic scalability and some capacity planning.

  <br/>

* **Statelessness**: Inherent for serverless, which means scalability is never a problem; state is maintained in an external service or resource. PaaS, containers and VMs can leverage HTTP, keep an open socket or connection for long periods of time, and store state in memory between calls.

  <br/>

* **High availability (HA) and disaster recovery (DR)**: Both are inherent in serverless with no extra effort and at no additional cost. The other models require additional cost and management effort. In the case of both VMs and containers, infrastructure can be restarted automatically.

* **Resource utilization**: Serverless is 100% efficient because there are no such things thing as idle capacity—it is invoked only upon request. All other models feature at least some degree of idle capacity.

  <br/>

* **Billing granularity and savings**: Serverless is metered in units of 100 milliseconds. PaaS, containers and VMs are typically metered by the hour or the minute.

 <br/>

### How can one get started with Vercel, and what are the main steps involved in deploying a serverless function using Vercel?

 <br/>

**Get started:** 

1. On the "New Project" page, under the "Import Git Repository" section, choose the account that you'd like to link a project from.
   
2. Find the repository in the list and select Import.
   
3. Vercel will automatically detect the framework and any necessary build settings. However, you can also configure the Project settings at this point including the build and development settings and Environment Variables. These can also be set later.
   
4. Press the Deploy button. Vercel will create the Project and deploy it based on the chosen configurations.
Enjoy the confetti!

5. To view your deployment, click on the Project in the dashboard and then click on the Domain. This page is now visible to anyone who has the URL.

 **Deploying a serverless function:**
 1. In your project directory, create a new file for your serverless function. The function should export a handler function that receives a request and returns a response. Here's a simple example of a serverless function using Python:
   
    <br/>
   
   ```
from http.server import BaseHTTPRequestHandler
from datetime import datetime
 
class handler(BaseHTTPRequestHandler):
 
  def do_GET(self):
    self.send_response(200)
    self.send_header('Content-type', 'text/plain')
    self.end_headers()
    self.wfile.write(str(datetime.now().strftime('%Y-%m-%d %H:%M:%S')).encode())
    return

   ```
   <br/>

   2. Deploy Serverless Function
   
   3. Test and Use Your Serverless Function: Once the deployment process is complete, Vercel will provide you with a unique URL for your serverless function.
   
   <br/>

### What are APIs, and how can they be utilized in Python applications to access and manipulate data from external sources?

**API** stands for **Application Programming Interface**. In essence, an API acts as a communication layer, or as the name says, an interface, that allows different systems to talk to each other without having to understand exactly what each other does.

<br/>

```

from http.server import BaseHTTPRequestHandler
from urllib import parse
import requests
 
class handler(BaseHTTPRequestHandler):
       def do_GET(self):

        s = self.path
        url_components = parse.urlsplit(s)
        query_strings_list = parse.parse_qsl(url_components.query)
        dic = dict(query_strings_list)
        print(dic)
        capital = dic.get("capital")
    

        if capital:
            url = "https://restcountries.com/v3.1/capital/"
            res = requests.get(url+capital)
            data = res.json()
            result = data[0]["name"]["common"]
            str = capital + " is the capital of " + result 

        self.send_response(200)
        self.send_header('Content-type','text/plain')
        self.end_headers()
        self.wfile.write(str.encode('utf-8'))
        return

```

<br/>

### What is the Requests library in Python, and how can it be used to interact with APIs by sending HTTP requests? Can you provide an example of a basic GET request using the Requests library?

<br/>

**What ?** 
Requests is an elegant and simple HTTP library for Python, built for human beings.

**Example:** See the previous question 