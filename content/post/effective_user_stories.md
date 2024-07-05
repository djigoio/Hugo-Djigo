---
title: "Effective User Stories: Enhancing Team Collaboration and Delivery"
date: 2024-07-04T12:00:00Z
draft: false
custom_description: In this article, we will delve into **what makes a user story rock-solid**, and why it is essential for your team's success. We will explore the key characteristics of high-quality user stories, provide practical tips for writing them, and discuss how to avoid common pitfalls.
custom_img_cover: https://i.imgur.com/hOYMdGw.png
post_url: www.djigo.dev/post/effective_user_stories/
---
## What are the user stories?

In the dynamic world of product development and engineering, **effective communication and collaboration are critical to a project's success**. User stories serve as the backbone of agile methodologies, providing a clear and concise way to capture user requirements and translate them into actionable tasks for the development team.
 
When done right, user stories can drive alignment, foster collaboration, and streamline the development process. However, crafting user stories that are truly "bullet-proof" requires a blend of art and science. It involves understanding the core principles of **effective storytelling**, embracing **best practices**, and continuously refining the process based on feedback and real-world experience.

## What will you learn

In this article, we will delve into **what makes a user story rock-solid**, and why it is essential for your team's success. We will explore the key characteristics of high-quality user stories, provide practical tips for writing them, and discuss how to avoid common pitfalls.

Whether you are a product manager, a developer, or a stakeholder, mastering the art of bullet-proof user stories will empower you to deliver products that truly resonate with your users, and will make your peer's life easier.

Also, we'll speak about a method called **Gherkin**, used for highly-technical tickets that are aimed to both devs and non-technical profiles.

![What's this?](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExNzF5aWliMnRxMWkyMHJkM3VoZzM0emo0b2RpancweWQ0emt5bXA4NiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/8079jlIfkJneWbyrdu/giphy.webp)

## Understanding User Stories

User stories are **concise**, simple descriptions of a feature told from the perspective of the end user. They focus on what the user needs and why. Typically, they follow a basic format:

**Template**: "As a [**type of user**], I want [**an action**] so that [**a benefit**]."

**Purpose**: To capture user requirements and facilitate clear communication between stakeholders and development teams.

## Characteristics of Bullet-Proof User Stories

- **Clarity**: Easy to understand with no ambiguity.
- **Conciseness**: Brief yet comprehensive enough to convey the necessary information.
- **Specificity**: Provides sufficient detail without being overly prescriptive.

These stories should follow the **INVEST** criteria, which stands for independent, negotiable, valuable, estimable, small, and testable.

### INVEST Criteria

- **Independent**: The story should stand alone, allowing it to be developed and delivered independently of other stories.
- **Negotiable**: Stories should be flexible and open to discussion and modification.
- **Valuable**:Each story should provide value to the user or customer.
- **Estimable**:The team should be able to estimate the effort required to complete the story.
- **Small**:The story should be small enough to be completed in a single iteration or sprint.
- **Testable**:There should be clear criteria to determine when the story is complete and meets the requirements.

Also, good acceptance criteria are key because they help the team and other developers grasp the fundamental technical details of a task.

## Acceptance Criteria

Acceptance criteria **specify the requirements that need to be fulfilled to meet the user's needs** as described in the user story. They provide a clear definition of done, helping to prevent misunderstandings and scope creep during development. Essentially, acceptance criteria outline the conditions under which the user story can be considered satisfactorily implemented and ready for testing and deployment.

### How Should Acceptance Criteria Be?
Acceptance criteria should be:

- **Specific**: Clearly define what needs to be achieved and what constitutes success.
- **Measurable**: Provide a way to objectively verify when the criteria are met.
- **Achievable**: Realistic and feasible within the project constraints.
- **Relevant**: Directly related to the user story and its intended outcome.
- **Time-bound**: Clearly state when the acceptance criteria should be fulfilled.

Overall, here's an example of a bad vs a good user story about the necessity of adding a new cookie banner for a promotional campaign, that will show specific content depending on wether the user accepts or not:

### Bad Example of a User Story

```
Title: Show Cookie Banner

User Story:

As a user,
I want a cookie banner,
so that cookies are handled.

Acceptance Criteria:
- Display a cookie banner.
```
Yeah, but, what should happen when user declines? How long should the cookies stay on the browser?, Should we keep showing it if the user accepts?

Above, you'd be failing the achieve most of the acceptance criteria and user story criteria (except for the Small one...)
 
### Good Example of a User Story

```
User Story:

As a new user that enters the website for the first time,
I want a cookie banner to be displayed to me,
so that cookies can be stored in my browser to determine what to display on the website during the promotional campaign.

Acceptance Criteria:

- Upon first visit, a prominent cookie banner is displayed at the bottom of the website (Check design files below).
- The banner includes options to "Accept" or "Decline" cookies.
- It remains visible until the user makes a choice.
- If the user clicks "Accept," cookies are stored in the browser to record their preference.
- If the user clicks "Decline," no cookies are stored, and the banner remains visible on subsequent visits.
- Component A, related to tracking order status, is shown only if the user accepts cookies.
- If cookies are declined, Component A remains hidden.
- The user's cookie preference is remembered across sessions and visits to the website.
- The banner does not reappear after the user has made a choice unless they clear their browser cookies.
- Ensure the cookie banner and options are accessible to all users, including those using assistive technologies.
- Ensure compliance with legal requirements for cookie consent and user privacy regulations. Link in the cookie banner should forward the user to https://web.xyz/legal on a new tab.
- Verify that the cookie banner appears correctly on different browsers and devices.
```
Here, you can see it's still small, concise, easier to estimate, specific, and testable.

![Better now](https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExdHVnNGtzOHJ6Mm1vbTdzZjl1aDZsb21lcWZsYzY4ZWFnaHppNmo0MyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/PqBh9miQvMQ2zamKJ2/giphy.webp)

Now, the promised prompts for creating good user stories using tools or models like GPT, Gemini, or Copilot. Always be as informative as possible, like so:

```
Delete everything from before. As if you were Senior Product Owner, Can you please generate a good user story following this format: 'As a [new user that entered the website for the first time], I want [a cookie banner to be displayed to the user] so that [we can store the cookies in the user's browser to decide what to show on the website]'? [The user story should be related to a new feature for a shopping website with a promotional campaign that allows users to track their order status. Component A should be shown only is user accepts the cookies] Please add an extensive and concise acceptance criteria for the developers to understand. Ask me if there is any doubt on what fields are we working, if any data or description is incomplete, on or anything relevant.
```

Be sure to adapt everything that's between the "[ ]" so it matches your story.

## The Gherkin Method

Gherkin is a structured language used to describe scenarios in a way that is **easy to understand by both technical and non-technical stakeholders**. It's primarily used in [BDD](https://cucumber.io/docs/bdd/) (a way for software teams to work that closes the gap between business people and technical people) to define acceptance criteria and specify how software should behave in various scenarios.

### When is Gherkin used?

Gherkin is typically used in agile environments, where collaboration between business analysts, developers, and testers is essential. It helps **ensure that everyone has a clear understanding of the expected behavior** of a feature or system.

A normal user story, as described earlier, typically follows a format that outlines the who, what, and why of a feature from a user's perspective. On the other hand, Gherkin is more structured and focuses on specifying the behavior of the software through scenarios written in a specific syntax.

### Characteristics of a Gherkin story

- **Structure**: Gherkin scenarios are structured using keywords like Feature, Scenario, Given, When, and Then, which provide clear steps and expected outcomes.

- **Human-Readable**: Gherkin scenarios are written in plain, understandable language that can be easily read and understood by both technical and non-technical stakeholders. 

- **Automation**: Scenarios written in Gherkin can often be directly used as automated tests. They can also be used as documentation.

### Structure explanation

#### Feature
The Feature keyword is used to define a high-level description of a feature or functionality that is being tested. It provides context about what aspect of the system the scenarios are related to.

```
Feature: Login Functionality
  As a user,
  I want to be able to log into the system,
  So that I can access my account and manage my profile.
```

#### Scenario

The Scenario keyword is used to define specific test scenarios or examples that illustrate how the system should behave under certain conditions. Each scenario typically represents a specific use case or user story.

```
Scenario: Successful Login
  Given the user is on the login page
  When the user enters valid credentials
  And clicks on the login button
  Then the user should be logged into their account
  And redirected to the dashboard page.
```

#### Steps: Given, When, Then, And, But

**Given**: Specifies the initial state or precondition of the scenario. It sets up the context in which the scenario takes place.

**When**: Describes the action or event that occurs that triggers the behavior being tested.

**Then**: Defines the expected outcome or result of the action specified in the When step. It verifies the expected behavior of the system.

**And, But**: These keywords are used to continue the previous step (Given, When, or Then) to add additional context or conditions as needed.


```
Scenario: Search for a Product
  Given the user is on the homepage
  When the user enters "smartphone" in the search bar
  And clicks on the search button
  Then the search results page should display relevant products
  And the user should be able to filter and sort the results.
```

### Optionals for Gherkin

**Background**: Optional Gherkin keyword used to define steps that are common to all scenarios within a feature file. It helps in setting up a consistent starting state for scenarios, reducing redundancy. [Read more here.](https://cucumber.io/docs/gherkin/reference/#background)

**Scenario Outline**: Optional Gherkin keyword used to define a template for scenarios that vary only in their inputs or data. It allows for parameterization of scenarios using placeholders, which are replaced with concrete values in each scenario instance. [Read more here.](https://cucumber.io/docs/gherkin/reference/#scenario-outline)


Overall, let's see what a complete Gherkin story should look like for the example from before

### Example of a Gherkin story

```
Feature: Cookie Consent Banner
  As a new user visiting the shopping website,
  I want to see a cookie banner
  So that my preferences can be recorded and I can view relevant promotional content.

  Scenario: Display Cookie Banner
    Given I am a new user
    When I visit the shopping website
    Then I should see a cookie banner with options to accept or decline cookies

  Scenario: Accept Cookies
    Given I am a new user
    And I see the cookie banner
    When I click on "Accept"
    Then cookies should be stored in my browser
    And I should be able to view promotional content related to the campaign

  Scenario: Decline Cookies
    Given I am a new user
    And I see the cookie banner
    When I click on "Decline"
    Then cookies should not be stored in my browser
    And Component A, which allows users to track their order status, should not be displayed
```

And now, a good AI prompt to generate the Gherkin story, remember to change what's inside the "[ ]":

```
Delete everything from before. As if you were Senior Product Owner, Can you please generate a good user story following the Gherkin format: 'As a [new user that entered the website for the first time], I want [a cookie banner to be displayed to the user] so that [we can store the cookies in the user's browser to decide what to show on the website]'? [The user story should be related to a new feature for a shopping website with a promotional campaign that allows users to track their order status. Component A should be shown only is user accepts the cookies]  Ask me if there is any doubt on what fields are we working, if any data or description is incomplete, on or anything relevant.
```
![That was nice](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExdnI1YXJ2angydmRydmRneHdxeHdycHlrZXFlZHp2MnRsNTYyMDh3bCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/PdGrB8Vq9pn16LR983/giphy.webp)

Mastering the creation of bullet-proof user stories is not just about following a template but understanding the nuances of effective communication and stakeholder alignment. By applying these principles, **teams can navigate complexities, mitigate risks, and deliver impactful solutions that resonate with users**.


Hope you enjoyed the article. Feel free to follow me on [Twitter](https://x.com/brownio_), or just check my website! 

**https://djigo.dev**
