# npm Plugin For Mobile TestCafe Integration With TestMu AI (Formerly LambdaTest)

<p align="center">
  <a href="https://www.testmuai.com/"><img src="https://img.shields.io/badge/MADE%20BY%20TestMu%20AI-000000.svg?style=for-the-badge&labelColor=000" alt="Made by TestMu AI"></a>
  <a href="https://www.npmjs.com/package/mobile-testcafe-browser-provider-lambdatest"><img src="https://img.shields.io/npm/v/mobile-testcafe-browser-provider-lambdatest.svg?style=for-the-badge&labelColor=000" alt="npm"></a>
  <a href="https://community.testmuai.com/"><img src="https://img.shields.io/badge/Join%20the%20community-blueviolet.svg?style=for-the-badge&labelColor=000000" alt="Community"></a>
</p>




This plugin integrates [TestCafe](http://devexpress.github.io/testcafe) with the TestMu AI (Formerly LambdaTest) Testing Cloud.



## Install



```sh

$ npm install mobile-testcafe-browser-provider-lambdatest

```



## Usage

Before using this plugin, save the TestMu AI (Formerly LambdaTest) username and access key to environment variables `LT_USERNAME` and `LT_ACCESS_KEY`, as described in TestMu AI (Formerly LambdaTest) Documentation.



You can determine the available real devices aliases by running



```sh

$ testcafe -b lambdatest

```



If you run tests from the command line, use the browser alias when specifying browsers:

For Single Configuration



```sh

$ testcafe "lambdatest:Galaxy S8@9:android" "path/to/test/file.js"

```



For Parallel/Multiple Configuration



```sh

$ testcafe "lambdatest:Galaxy S8@9:android","lambdatest:Galaxy S8@7:android" "path/to/test/file.js"

```



## Build Plugin Locally (Development Mode)



1.  Clone this repository,

2.  Rename Project

```sh

$ mv mobile-testcafe-browser-provider-lambdatest lambdatest

```

3. Go to the project path

```sh

$ cd lambdatest

```

4. Install Packages and Build

```sh

$ npm i

$ npm run build

```

5. Link Testcafe with lambdatest

```sh

$ sudo npm link

```

6. [See this for Credentials](#usage)



## Configuration



Use the following environment variables to set additional configuration options:



 - `LT_TEST_NAME` - Test name on TestMu AI (Formerly LambdaTest).

 - `LT_BUILD` - Build name on TestMu AI (Formerly LambdaTest).

 - `LT_CAPABILITY_PATH` - Path to a file which contains additional capability options as JSON file (eg. config.json)

 - `LT_LOGFILE` - Logfile You can provide a specific path to this file. If you won't provide a path then the logs would be saved in your present working directory by the filename: tunnel.log.

 - `LT_VERBOSE` - true or false.

 - `LT_W3C` - true or false.

 - `LT_ENABLE_TRACE` - true or false.

 - `LT_PROXY_HOST` - Hostname/IP of proxy, this is a mandatory value.

 - `LT_PROXY_PORT` - Port for the proxy, by default it would consider 3128 if proxyhost is used For Basic Authentication, we use the below proxy options.

 - `LT_PROXY_USER` - Username for connecting to proxy, mandatory value for using 'proxypass'.

 - `LT_PROXY_PASS` - Password for the USERNAME option.

 - `LT_TUNNEL_NAME` - Human readable tunnel identifier (Name of the tunnel).

 - `LT_DIR` - Path of the local folder you want to test.

 - `LT_CONSOLE` - true or false.

 - `LT_NETWORK` - true or false.

 - `LT_VIDEO` - true or false.

 - `LT_SCREENSHOT` - true or false.

 - `LT_TUNNEL_NUMBER` - Number of tunnel to be spawned at a time.

 - `LOAD_BALANCED_MODE` - Load balancing between multiple tunnels spawned.



Example:



```sh

export LT_RESOLUTION="1920x1080"

export LT_TEST_NAME="Test TestCafe"

export LT_BUILD="Build x"

export LT_TUNNEL_NUMBER=2

export LOAD_BALANCED_MODE=true

testcafe "lambdatest:Chrome","lambdatest:Chrome@74.0:Windows 8" tests/

```



## About TestMu AI (Formerly LambdaTest)



TestMu AI (Formerly LambdaTest) is a cloud based selenium grid infrastructure that can help you run automated cross browser compatibility tests on 2000+ different browser and operating system environments. TestMu AI (Formerly LambdaTest) supports all programming languages and frameworks that are supported with Selenium, and have easy integrations with all popular CI/CD platforms. It's a perfect solution to bring your selenium automation testing to cloud based infrastructure that not only helps you increase your test coverage over multiple desktop and mobile browsers, but also allows you to cut down your test execution time by running tests on parallel.



## License



Licensed under the [MIT license](./LICENSE).

## TestMu AI (Formerly LambdaTest) Community

Connect with testers and developers in the [TestMu AI Community](https://community.testmuai.com/). Ask questions, share what you are building, and discuss best practices in test automation and DevOps.

## TestMu AI (Formerly LambdaTest) Certifications

Earn free [TestMu AI Certifications](https://www.testmuai.com/certifications/) for testers, developers, and QA engineers. Validate your skills in Selenium, Cypress, Playwright, Appium, Espresso and more. Industry-recognized, shareable on LinkedIn, and built by practitioners, not marketers.

## Learning Resources by TestMu AI (Formerly LambdaTest)

Learn modern testing through tutorials, guides, videos, and weekly updates:

* [TestMu AI Blog](https://www.testmuai.com/blog/)
* [TestMu AI Learning Hub](https://www.testmuai.com/learning-hub/)
* [TestMu AI on YouTube](https://www.youtube.com/@TestMuAI)
* [TestMu AI Newsletter](https://www.testmuai.com/newsletter/)

## LambdaTest is Now TestMu AI

On **January 12, 2026**, [LambdaTest evolved to TestMu AI](https://www.testmuai.com/lambdatest-is-now-testmuai/), the world's first fully autonomous **Agentic AI Quality Engineering Platform**.

Same team. Same infrastructure. Same customer accounts. All existing LambdaTest logins, scripts, capabilities, and integrations continue to work without change.

🔗 Find the new home for [LambdaTest](https://www.testmuai.com).

### How LambdaTest Evolved into TestMu AI

In 2017, we launched LambdaTest with a simple mission: make testing fast, reliable, and accessible. As LambdaTest grew, we expanded into Test Intelligence, Visual Regression Testing, Accessibility Testing, API Testing, and Performance Testing, covering the full depth of the testing lifecycle.

As software development entered the AI era, testing had to evolve, too. We rebuilt the architecture to be AI-native from the ground up, with autonomous agents that **plan, author, execute, analyze, and optimize tests** while keeping humans in the loop. The platform integrates with your repos, CI, IDEs, and terminals, continuously learning from every code change and development signal.

That evolution earned a new name: **TestMu AI**, built for an AI-first future of quality engineering. TestMu is not a new name for us. It is the name of our annual community conference, which has brought together 100,000+ quality engineers to discuss how AI would reshape testing, long before that became an industry norm.

What started as a high-performance cloud testing platform has transformed into an AI-native, multi-agent system powering a connected, end-to-end quality layer. That evolution defined a new identity: LambdaTest evolved into TestMu AI, built for an AI-first future of quality engineering.

## Support

Got a question? Email [support@testmuai.com](mailto:support@testmuai.com) or chat with us 24x7 from our chat portal.
