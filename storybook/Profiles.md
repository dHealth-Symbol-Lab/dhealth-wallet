#### Feature: Initial software landing page
  As a user, I want to see the profile creation page or the log-in page, so that I can activate a profile.

- [ ] Scenario: No profile available in database (fresh install)
```gherkin
  Given a user opens the software
  When the user did not previously create a Profile.
  Then the import strategy page should be displayed
```

- [ ] Scenario: Profile(s) exist in database
```gherkin
    Given a user opens the software
    When the user previously created a Profile.
    Then the Dashboard should be displayed
```

#### Feature: Import strategy page
  As a user, I want to see the profile creation and import strategy page, so that I can select a Profile creation strategy.

- [ ] Scenario: Profile creation strategy selected
```gherkin
    Given a user selects the creation profile strategy
    Then the Profile creation form should be displayed
```

- [ ] Scenario: Profile import strategy selected
```gherkin
    Given a user selects the import profile strategy
    Then the Profile import form should be displayed
```

#### Feature: Profile creation page - Step 1 (Profile info)
  As a user, I want to see the profile creation form, so that I can create a new Profile.

- [ ] Scenario: Invalid profile name input
```gherkin
    Given a user sees the profile creation form
    When the user inputs an invalid profile name, e.g. `#invalid`
    Then an error notification should be displayed
```

- [ ] Scenario: Invalid password confirmation
```gherkin
    Given a user sees the profile creation form
    When the user inputs an invalid password confirmation
    Then an error notification should be displayed
```

- [ ] Scenario: Invalid password hint
```gherkin
    Given a user sees the profile creation form
    When the user inputs a password hint that contains the password
    Then an error notification should be displayed
```

- [ ] Scenario: Valid form input is submitted
```gherkin
    Given a user sees the profile creation form
    When the user inputs valid values in the form
    Then the Mnemonic passphrase generation page should be displayed
```

