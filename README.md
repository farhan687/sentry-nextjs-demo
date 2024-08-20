This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

Follow following steps to reproduce the issue

## Issue

[thirdPartyErorFilterIntegration](https://docs.sentry.io/platforms/javascript/guides/hapi/configuration/filtering/#using-thirdpartyerrorfilterintegration) issue with nextjs application.

## Sentry working fine without thirdPartyErrorFilterIntegration

Set sentry related values in config.js file

```bash
npm i
npm run build
npm run start
```

Open [sentry-example-page](http://localhost:3719/sentry-example-page) with your browser to see the result.

Click on Throw Frontend error button, new issue is created on sentry project.

## Sentry not creating new issues with thirdPartyErrorFilterIntegration

1. Set sentry related values in config.js file
2. Uncomment line 30-41 in sentry.client.config.ts

```bash
npm i
npm run build
npm run start
```

Open [sentry-example-page](http://localhost:3719/sentry-example-page) with your browser to see the result.

Click on Throw Frontend error button, new issue is not created on sentry project.
