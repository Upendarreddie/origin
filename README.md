# origin
 import { test, expect } from '@playwright/test';
     test('Verify login with valid credentials', async ({page})=> { 
     await page.goto("https://www.instagram.com/accounts/login/?hl=en")
     await page.locator("input[aria-label='Phone number, username, or email']").fill("upendar_reddy")
     await page.locator("input[aria-label='Password']").fill("Upendar@88")
     await page.locator("form#loginForm>div>div:nth-of-type(3)").click()
     await expect(page).toHaveURL("https://www.instagram.com/accounts/login/?hl=en") 
     await page.close();
})
