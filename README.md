<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
    <img src="resources/images/logo.png" alt="Logo" width="80" height="80">

<h3 align="center">Digital Nomad/h3>

  <p align="center">
    Find Your Destination
    <br />
    <br />
    <br />
    <a href="#usage">View Demo</a>
  </p>
</div>



<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

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

<p align="right">(<a href="#readme-top">back to top</a>)</p>

---

## Build Tools

* Java
* Javascript
* HTML
* CSS
* Docker
* AWS DynamoDB
* AWS CloudFront
* AWS CloudFormation

<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Initial Setup

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
  
After doing all of this, you will have a server running on port `8000` - you can access it by going to [http://localhost:8000](http://localhost:8000) in your browser.

To stop either the local backend (the `sam local...` command) or local frontend (the `npm run...`) command, simply press `Ctrl-C` in the terminal where the process is running.

**SONGS TABLE**
- `TITLE: The Yellow Submarine ARTIST: The Beatles`
- `TITLE: The Lonely Island ARTIST: I'm On A Boat`
- `TITLE: Come Sail Away ARTIST: Styx`
- `TITLE: Sailing ARTIST: Christopher Cross`
- `TITLE: Rock The Boat ARTIST: Hues Corporation`

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage


[Party Playlist Demo](https://user-images.githubusercontent.com/57022409/209223943-2804c2cd-f6af-41b7-abe0-5774fd682b4a.mp4)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Alex Murillo - alex.d.murillo@protonmail.com

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/Traversg/Party_Playlist.svg?style=for-the-badge
[contributors-url]: https://github.com/Traversg/Party_Playlist/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo_name.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo_name/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo_name.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo_name/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo_name.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo_name/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo_name.svg?style=for-the-badge
[license-url]: https://github.com/github_username/repo_name/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/travers-geoffray/
[product-screenshot]: resources/images/home-page.png
[DynamoDb]: https://img.shields.io/badge/AWS_DynamoDB-yellow?style=for-the-badge&logo=amazondynamodb&logoColor=4053D6
[DynamoDb-url]: https://aws.amazon.com/dynamodb/
[Lambda]: https://img.shields.io/badge/AWS_Lambda-blue?style=for-the-badge&logo=awslambda&logoColor=FF9900
[Lambda-url]: https://aws.amazon.com/lambda/
[API Gateway]: https://img.shields.io/badge/AWS_API_Gateway-black?style=for-the-badge&logo=amazonapigateway&logoColor=FF4F8B
[Gateway-url]: https://aws.amazon.com/api-gateway/
[JavaScript]: https://img.shields.io/badge/JavaScript-20232A?style=for-the-badge&logo=javascript&logoColor=61DAFB
[JavaScript-url]: https://javascript.com/
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[Java]: https://img.shields.io/badge/Java-darkgreen?style=for-the-badge
[Java-url]: https://java.com/
[AWS CloudFront]: https://img.shields.io/badge/AWS_CloudFront-orange?style=for-the-badge
[Cloudfront-url]: https://aws.amazon.com/cloudfront/
[AWS CloudFormation]: https://img.shields.io/badge/AWS_CloudFormation-red?style=for-the-badge
[Cloudformation-url]: https://aws.amazon.com/cloudformation/
