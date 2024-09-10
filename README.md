# Overwrite API

[![Node.js CI](https://github.com/kazizehsan/overwrite-backend/actions/workflows/node.js.yml/badge.svg)](https://github.com/kazizehsan/overwrite-backend/actions/workflows/node.js.yml)

## Table of Contents

- [Manual Installation](#manual-installation)
- [AWS Lambda Deployment](#aws-lambda-deployment)
- [License](#license)

## Manual Installation

Clone the repo.

Install the dependencies:

```bash
yarn install
```

Set the environment variables:

```bash
cp .env.example .env
```

Open .env and modify the environment variables (if needed).

Make sure you have MongoDB running locally. Then:

```bash
yarn dev
```

## AWS Lambda Deployment

Make sure you have AWS and SAM CLIs installed locally.

Make sure you have MongoDB running on the cloud.

Create AWS Secrets Manager secrets like so:

- overwrite/prod:jwt_secret
- overwrite/prod:mongodb_url

Finally, run the following. **_Warning_**, this will create an S3 bucket and a CloudFormation Stack on your configured AWS account.

```bash
yarn setup
```

## License

[MIT](LICENSE)
