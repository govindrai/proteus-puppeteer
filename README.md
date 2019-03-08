# Proteus-Puppeteer

This repo contains a chromium binary, version 73.0.3679.0, that works with AWS Lambda's Linux AMI
It also includes puppeteer-core as a depedency, a tool used to interface with Chromium using the devtools protocol

## Usage

*Installation*

```bash
npm install proteus-puppeteer --save
```

Add this module as a dependency to your lambda and package it up and upload to Lambda. 
Remember the 50 mb package size limit. 
If your package size is larger, you will need to zip up your project to S3 and reference your lambda from there (up to 250 mb).

To use this binary with Puppeteer, simply point your puppeteer executable launch path to the "headless-shell" binary located in this node module.
