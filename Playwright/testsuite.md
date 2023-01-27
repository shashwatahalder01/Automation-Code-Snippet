# how to handle test for experimental/upcoming feature on test suite

        

    test('test upcoming feature', async ({ request }) => {
    !!process.env.CI && test.fail(!!process.env.ADMIN, 'Not Implemented Yet')
    });


test.fail() means expecting test to be failed

test will fail as featured isn't merged yet, but  will not be marked as failed in test-result and suite will pass. After the feature is merged with the repo, test will no longer be fail but as we are expecting this test to be failed, will be marked as failed in test result and suite will fail.
then we can remove the test.fail() line
