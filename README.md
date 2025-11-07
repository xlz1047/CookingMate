# AND101 Milestone 1 - CookingMate

Submitted by:
- **Caleb Nebiyu**
- **Umme Raisah**
- **Shreeya Gupta**
- **Taaruni Ananya**
- **Xin Zheng**

Time spent: **8** hours spent in total

## Summary

This document provides an overview, project spec, and wireframes for our team's capstone project: An app that **uses AI-powered conversations to help users discover personalized recipes and organize them in a beautiful recipe book**.

If we had to describe this milestone in three (3) emojis, they would be: 🤖🍳📚

## Milestone Requirements

The following REQUIRED features are completed:

- [x] Creation of GitHub Organization and Group Project Repo
- [x] Updated Course Portal group info with Group Name and App Description

The following REQUIRED files are included:

- [x] Included 📄 `brainstorming.md`, which contains:
  - [x] Our initial brainstorming ideas (6+ ideas)
  - [x] 5-category evaluation of our top 3 ideas
  - [x] Final app idea chosen
- [x] Included 📄 `project_spec.md`, which contains:
  - [x] App Overview: Description and evaluation
  - [x] App Spec: User features, Chosen API(s), User Interactions
  - [x] Wireframe image(s)

The following BONUS features are implemented:

- [ ] Added digital wireframe/mockup image(s)
- [ ] Added a Video/GIF of an interactive prototype

The following EXTRA features are implemented:

- [x] Detailed API research with free tier options identified
- [x] Technical architecture planning (Kotlin, MVVM, Jetpack Compose)
- [x] Comprehensive user interaction flow documentation
- [x] Stretch features roadmap for future development

## Notes

### Planning Insights

Our team spent considerable time evaluating different app ideas across the 5 evaluation categories. CookingMate emerged as the clear winner because:

1. **Strong Mobile Experience**: Unlike recipe websites, our app leverages mobile-specific features like camera integration, voice input, and offline access that make it truly native
2. **Universal Appeal**: Everyone eats, making our market huge and well-defined
3. **Daily Habit Potential**: Users engage multiple times per day for meal planning
4. **Achievable Scope**: We can build a valuable MVP with just AI chat + recipe book in our timeline

### Technical Decisions

- **AI API Choice**: We're evaluating OpenChat 3.6 8B API, Claude API, and GPT API based on cost, response quality, and ease of integration
- **Recipe Data**: Spoonacular API selected for its comprehensive free tier (150 requests/day) and rich recipe metadata
- **Architecture**: MVVM pattern chosen for clean separation of concerns and testability
- **UI Framework**: Jetpack Compose selected for modern, declarative UI development

### Challenges Anticipated

1. Balancing AI API costs within free tier limits during development
2. Creating smooth, responsive chat interface with embedded rich media
3. Optimizing recipe image loading for performance
4. Designing intuitive navigation between chat and recipe book

### Next Steps

For Milestone 2, we'll focus on:
- Setting up project structure and architecture
- Implementing basic chat UI with Jetpack Compose
- Integrating AI API for recipe queries
- Creating recipe detail screen with ingredients display
- Setting up Room database for saved recipes

We're excited to build an app that solves a real daily problem in an innovative way!
