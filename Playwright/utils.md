## File Upload

    // Select one file
    await page.getByLabel('Upload file').setInputFiles('myfile.pdf');

    // Select multiple files
    await page.getByLabel('Upload files').setInputFiles(['file1.txt', 'file2.txt']);

    // Remove all the selected files
    await page.getByLabel('Upload file').setInputFiles([]);

    // Upload buffer from memory
    await page.getByLabel('Upload file').setInputFiles({
    name: 'file.txt',
    mimeType: 'text/plain',
    buffer: Buffer.from('this is test')
    });





## Click and wait for network request to return 200 response

    let [response] = await Promise.all([    
            page.waitForResponse(resp => resp.url().includes('/dokan-driver/v1/delivery') && resp.status() === 200),
            page.getByRole('option', { name: status }).click()
            ])

## Assert element is visible [waiting for the element to be visible]

    await expect(page.locator('locator').toBeVisible()



## Screen-short

await page.screenshot({ path: 'screenshot.png' });

#### Full page
await page.screenshot({ path: 'screenshot.png', fullPage: true });

