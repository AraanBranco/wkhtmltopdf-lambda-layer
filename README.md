## WkHtmlToPDF Lambda Layer
---


## Installation

Install npm
```
npm install
```

Deploy your layer:
```
sls deploy
```

## Usage

Create you function in serverless:
```yml
youFunction:
  handler: handler.youFunction
  events:
    - http:
      path: /my-endpoint
      method: post
      cors: true
  environment:
    FONTCONFIG_PATH: /opt/fonts # You need this env for your lambda
  layers:
    - arn:aws:lambda:us-east-1:xxxxxx:layer:wkhtmltopdf-lambda-layer:1
```
