




## Record Video

- 'off' - Do not record video.
- 'on' - Record video for each test.
- 'retain-on-failure' - Record video for each test, but remove all videos from successful test runs.
- 'on-first-retry' - Record video only when retrying a test for the first time.


```
    import type { PlaywrightTestConfig } from '@playwright/test'
    const config: PlaywrightTestConfig = {
    use: {
        video: 'on-first-retry',
    },
    };
    export default config;
```

```
    import type { PlaywrightTestConfig } from '@playwright/test';
    const config: PlaywrightTestConfig = {
    use: {
        video: {
        mode: 'on-first-retry', 
        size: { width: 640, height: 480 }
        }
    },
    };
    export default config;
```


```
const path = await page.video().path();
```