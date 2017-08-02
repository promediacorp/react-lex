# react-lex

ReactJS AWS Lex Chat Component

## Demo

[http://react-lex.s3-website-us-east-1.amazonaws.com/
](http://react-lex.s3-website-us-east-1.amazonaws.com/)

<img src="https://thumbs.gfycat.com/ShabbyCourageousFalcon-size_restricted.gif" width="50%">

## Prerequisites
The AWS Javascript SDK for the browser is required. This package will install the entire SDK, but all you need is AWS.LexRuntime and AWS.CognitoIdentity. We recommend you build your own version of the AWS SDK for JavaScript using the [builder](https://sdk.amazonaws.com/builder/js/) to include only the services you need.

You will need to set up an AWS Cognito federated identity pool, and pass the IdentityPoolId as props to the component. Be sure to enable access to unauthenticated identities, and modify the IAM roles to allow access to Amazon Lex. From the IAM console, attach the AmazonLexRunBotsOnly and AmazonPollyReadOnlyAccess policies. [This blog post](https://aws.amazon.com/blogs/ai/greetings-visitor-engage-your-web-users-with-amazon-lex/) walks through the process in detail. 



## Installing react-lex

```
npm install --save react-lex
```

## Using the Component


Example:

```js
import LexChat from "react-lex";

class App extends Component {
  render() {
        <LexChat botName="OrderFlowers"
                 IdentityPoolId="us-east-1:7292b8c0-56f1-4441-b2a6-xxxxxxxxxxxx"
                 placeholder="Placeholder text"
                 style={{position: 'absolute'}}
                 backgroundColor="#FFFFFF"
                 height="430px"
                 headerText="Chat with our awesome bot" />
  }
}
export default App;
```
* Your botname (ie. "OrderFlowers") is a required prop.
* Your IdentityPoolId is a required prop.

##License

The MIT License (MIT)

Copyright (c) 2017.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
