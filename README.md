## Problem

[thirdPartyErorFilterIntegration](https://docs.sentry.io/platforms/javascript/guides/hapi/configuration/filtering/#using-thirdpartyerrorfilterintegration) feature is not working with nextjs application.

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
2. Uncomment [line 30-41 in sentry.client.config.ts](https://github.com/farhan687/sentry-nextjs-demo/blob/main/sentry.client.config.ts#L30-L41)

```bash
npm i
npm run build
npm run start
```

Open [sentry-example-page](http://localhost:3719/sentry-example-page) with your browser to see the result.

Click on Throw Frontend error button, new issue is not created on sentry project.
