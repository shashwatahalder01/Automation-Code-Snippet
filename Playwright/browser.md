<style>
r { color: Red }
o { color: Orange }
g { color: Green }
</style>



## Browser context

### Chromium

    import { chromium, FullConfig } from '@playwright/test'

    const browser = await chromium.launch()
    const page = await browser.newPage()
    // test code
    await page.close()
    await browser.close()