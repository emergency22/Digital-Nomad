<a href="https://github.com/emergency22/Digital-Nomad/graphs/contributors"><img alt="GitHub contributors" src="https://img.shields.io/badge/-Contributors-orange"></a>
<a href="https://www.linkedin.com/in/alexdmurillo/"><img alt="LinkedIn" src="https://img.shields.io/badge/-LinkedIn-brightgreen"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
    <img src="resources/images/logo.png" alt="Logo" width="80" height="80">

<h3 align="center">Digital Nomad</h3>

  <p align="center">
    Find Your Destination
    <br />
  </p>
</div>

---

## Synopsis

<img src="resources/images/frontpage.png">

Digital Nomad is a "mid-stone" group project at Nashville Software School. Contributors to this project include Alex Murillo, Erika Smith, Matt Marotta, and Steve Winters.

Digital Nomad is a service that allows users to search for travel destinations based on criteria such as access to beaches, night life, etc. Users are then provided a list of potential destinations, which they can then save for later viewing at a provided URL.

---

## Lessons Learned

Concise and detailed initial planning will pay dividends. Particularly if the project planning is well thought out. This will help avoid future confusion and the need to reinvent the wheel. This also speaks to breaking down tasks into manageable pieces.

While I did have some limited experience, the front end work was challenging in a good way, and helped to further develop my skills in that area. The experience I had with Java also helped me understand Javascript with its similar syntax.

I also discovered that it may be best to have team members focus on particular areas as opposed to switching roles. I feel we may have been more efficient had we "specialized" in certain areas.

---

## Build Tools

* <img alt="LinkedIn" src="https://img.shields.io/badge/-Java-red"></a>
* <img alt="LinkedIn" src="https://img.shields.io/badge/-Javascript-orange"></a>
* <img alt="LinkedIn" src="https://img.shields.io/badge/-HTML-blue"></a>
* <img alt="LinkedIn" src="https://img.shields.io/badge/-CSS-green"></a>
* <img alt="LinkedIn" src="https://img.shields.io/badge/-Docker-9cf"></a>
* <img alt="LinkedIn" src="https://img.shields.io/badge/-AWS%20DynamoDB-ff69b4"></a> 
* <img alt="LinkedIn" src="https://img.shields.io/badge/-AWS%20CloudFront-yellowgreen"></a>
* <img alt="LinkedIn" src="https://img.shields.io/badge/-AWS%20CloudFormation-purple"></a>

---

## Setup

1. Use an Amazon AWS account.
2. Install AWS CLI. [Documentation](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
3. Install AWS SAM CLI. [Documentation](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/install-sam-cli.html)
4. Install NodeJS to run the npm commands below.

- For Windows / WSL users:
```shell
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
```
- For Mac users:
```shell
brew install node
```

### Backend Setup via Lambda Service
1. Build the Java code: `sam build`
2. Create an S3 bucket: `aws s3 mb s3://YOUR_BUCKET`
3. Deploy the SAM template: `sam deploy --s3-bucket BUCKET_FROM_ABOVE --parameter-overrides S3Bucket=BUCKET_FROM_ABOVE FrontendDeployment=local`
   > **NOTE:** _Yes you have to provide the same S3 bucket name twice. Yes this is annoying._
4. Run the local API: `sam local start-api --warm-containers LAZY`


### Frontend Setup
1. CD into the web directory: `cd web`
2. Install dependencies : `npm install`
3. Run the local server: `npm run run-local` 
- > **NOTE:** Only songs found in the song table can be added to the playlist.
  
After the steps above, you will have a server running on port `8000` - you can access it via [http://localhost:8000](http://localhost:8000) in your web browser.

---

## Contact

Alex Murillo - alex.d.murillo@protonmail.com
<br>
<a href="https://www.linkedin.com/in/alexdmurillo/"><img alt="LinkedIn" src="https://img.shields.io/badge/-LinkedIn-brightgreen"></a>


