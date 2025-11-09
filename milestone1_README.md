# AND101 Milestone 1 - CookingMate

Submitted by:
- **Caleb Nebiyu**
- **Umme Raisah**
- **Shreeya Gupta**
- **Taaruni Ananya**
- **Xin Zheng**

Time spent: **8** hours spent in total

## Summary

This document provides an overview, project spec, and wireframes for our team's capstone project: An app that **uses AI-powered conversations to help users discover personalized recipes and view detailed cooking instructions**.

If we had to describe this milestone in three (3) emojis, they would be: 🤖🍳📱

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
- [x] Simplified scope for achievable MVP

## Notes

### Planning Insights

Our team spent considerable time evaluating different app ideas across the 5 evaluation categories. CookingMate emerged as the clear winner because:

1. **Strong Mobile Experience**: Unlike recipe websites, our app leverages conversational AI for natural recipe discovery while cooking
2. **Universal Appeal**: Everyone eats, making our market huge and well-defined
3. **Daily Habit Potential**: Users engage multiple times per week for meal planning
4. **Achievable Scope**: We simplified to just two core screens - AI chat and recipe detail view

### Scope Simplification

After initial planning, we made the strategic decision to simplify our MVP to focus on the core value proposition:

**Original Plan:**
- AI chatbot for recipe discovery ✅
- Recipe detail view with ingredients and steps ✅
- Recipe book for saving favorites ❌ (moved to V2)
- Search functionality ❌ (moved to V2)
- Ingredient checkboxes ❌ (moved to stretch features)

**Simplified MVP (V1):**
- **Screen 1**: AI Chatbot - conversational recipe discovery with embedded recipe cards
- **Screen 2**: Recipe Detail - full ingredients list and step-by-step instructions with tab navigation

This focused approach allows us to:
- Build a polished, fully functional MVP within our timeline
- Test the core user flow: discovery → view → cook
- Validate whether users find value in AI-powered recipe discovery
- Establish clean architecture for future feature additions

### Technical Decisions

- **AI API Choice**: Evaluating OpenChat 3.6 8B API, Claude API, and GPT API based on cost, response quality, and integration complexity
- **Recipe Data**: Spoonacular API selected for its comprehensive free tier (150 requests/day) and rich recipe metadata
- **Architecture**: MVVM pattern chosen for clean separation of concerns and testability
- **UI Framework**: Jetpack Compose selected for modern, declarative UI development
- **No Database Needed**: Recipes are displayed in-memory during chat session, no persistence required for MVP

### Challenges Anticipated

1. Balancing AI API costs within free tier limits during development
2. Creating smooth, responsive chat interface with embedded recipe cards
3. Optimizing recipe image loading for performance
4. Passing recipe data efficiently between chat and detail screens
5. Designing intuitive conversation flow with the AI

### Key User Flow

```
User Opens App
    ↓
Chat Screen (AI Welcome)
    ↓
User: "What can I make with chicken?"
    ↓
AI: Shows recipe card with image
    ↓
User taps "View Recipe"
    ↓
Recipe Detail Screen (Ingredients Tab)
    ↓
User switches to Steps Tab
    ↓
User follows cooking instructions
    ↓
User taps Back → Returns to Chat
    ↓
User asks for another recipe
```

### Next Steps

For Milestone 2, we'll focus on:
- Setting up project structure with MVVM architecture
- Implementing chat UI with Jetpack Compose
- Integrating AI API for conversational queries
- Integrating Spoonacular API for recipe data
- Creating recipe card composable for chat display
- Building recipe detail screen with tab navigation
- Implementing smooth navigation between screens
- Testing with real recipe queries and user flows

### Why This Simplified Approach Works

1. **Clear Value Proposition**: Users immediately understand - ask for recipes, get detailed instructions
2. **No Learning Curve**: Simple two-screen app with intuitive navigation
3. **Mobile-First**: Optimized for cooking in the kitchen with conversational discovery
4. **Foundation for Growth**: Clean architecture allows easy addition of save/search features in V2
5. **Testable**: Can validate core hypothesis with real users cooking recipes

We're excited to build a focused, polished app that solves a real daily problem in an innovative way! The simplified scope ensures we deliver quality over quantity and create a solid foundation for future enhancements.
