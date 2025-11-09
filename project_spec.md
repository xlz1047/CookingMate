# **CookingMate**

## Table of Contents

1. [App Overview](#App-Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
1. [Build Notes](#Build-Notes)

## App Overview

### Description 

CookingMate is an AI-powered recipe assistant that helps users discover recipes through natural conversation. Users chat with an AI to find recipes based on available ingredients, dietary preferences, or meal ideas, then tap to view detailed recipe information including ingredients and step-by-step cooking instructions.

### App Evaluation

- **Category:** Food & Drink / Lifestyle
- **Mobile:** Mobile is essential for accessing the AI chatbot and recipes while actively cooking in the kitchen. Users get real-time recipe suggestions through conversational interaction and can reference recipe details hands-free while preparing meals.
- **Story:** Eliminates the daily "What should I cook?" decision fatigue by making recipe discovery conversational and personalized. Instead of endless scrolling through recipe websites, users simply ask the AI and get immediate suggestions with full cooking details.
- **Market:** Anyone who cooks at home could utilize this app - approximately 70% of adults cook regularly. Appeals to busy professionals needing quick dinner ideas, college students learning to cook, and home cooks looking for meal inspiration.
- **Habit:** Users interact with the chatbot multiple times per week when planning meals. Daily use during active cooking periods when deciding what to make and following recipe instructions.
- **Scope:** V1 focuses on two core screens: AI chatbot for recipe discovery and recipe detail view with ingredients and steps. This simplified scope is achievable and testable with real users cooking meals. Future versions could add recipe saving, search, and organization features.

## Product Spec

### 1. User Features (Required and Optional)

**Required Features (MVP):**

- **AI Chatbot Interface** - Users can type natural language queries to discover recipes
- **Recipe Suggestions** - AI responds with personalized recipe recommendations based on queries
- **Recipe Preview Cards** - Visual recipe cards displayed in chat with images, time, and difficulty
- **View Recipe Details** - Tap "View Recipe" button to navigate to recipe detail screen
- **Recipe Hero Image** - Large appetizing photo of the finished dish
- **Recipe Metadata** - Display cooking time, servings, and difficulty level with clear icons
- **Ingredients Tab** - List of all required ingredients with quantities
- **Steps Tab** - Numbered step-by-step cooking instructions
- **Tab Navigation** - Switch between Ingredients and Steps views
- **Back Navigation** - Return to chatbot from recipe detail screen

**Stretch Features (Future Versions):**

- **Save Recipes** - Bookmark recipes to a personal collection
- **Recipe Book** - View grid of saved recipes
- **Search Functionality** - Search through saved recipes
- **Voice Input** - Speak queries instead of typing
- **Ingredient Checklist** - Interactive checkboxes to mark off ingredients
- **Serving Adjustment** - Scale recipe ingredients based on servings
- **Share Recipes** - Share recipe details with friends


### 2. Chosen API(s)

- **OpenChat 3.6 8B API / Anthropic Claude API / OpenAI GPT API**
  - Powers conversational AI chatbot for recipe queries
  - Processes natural language to understand user intent
  - Generates personalized recipe recommendations
  - Provides conversational responses and follow-up suggestions
  
- **Spoonacular API** (https://spoonacular.com/food-api)
  - Recipe search and filtering (10,000+ recipes)
  - Detailed recipe information (ingredients, instructions, nutrition)
  - Recipe images and metadata
  - Ingredient analysis and substitutions
  - Free tier: 150 requests/day (sufficient for MVP testing)
  
- **Alternative: Edamam Recipe Search API** (https://www.edamam.com/)
  - 2.3 million+ recipes from various sources
  - Detailed nutritional information
  - Dietary and health filters
  - Free tier: 10 requests/min, 10,000/month

### 3. User Interaction

Required Feature

- **User opens app**
  - => App launches directly to AI Chat screen
  - => AI displays welcome message: "Hi! I'm your cooking assistant. What would you like to make today?"
  - => Input field ready for user query at bottom
  
- **User types "What can I make with chicken?"**
  - => AI processes query and displays thinking indicator (loading animation)
  - => AI responds with conversational text: "Great question! Here's a popular recipe for you:"
  - => Recipe card appears in chat with:
    - Large appetizing food photo
    - Recipe title (e.g., "Classic Lemon Herb Roasted Chicken")
    - Quick info: "1 hr 15 min • Easy"
    - Teal "View Recipe" button
  
- **User taps "View Recipe" button on recipe card**
  - => App navigates to Recipe Detail screen
  - => Screen displays:
    - Hero image of finished dish at top
    - Recipe title below image
    - Three info cards showing: Total Time (1 hr 15 min), Servings (4 people), Difficulty (Easy)
    - Tab navigation with "Ingredients" and "Steps" tabs
    - "Ingredients" tab selected by default
  
- **User views Ingredients tab**
  - => Displays complete list of ingredients with quantities:
    - "Whole Chicken - 1 (about 4 pounds)"
    - "Lemons - 2, halved"
    - "Fresh Rosemary - 4 sprigs"
    - "Olive Oil - 2 tbsp"
  - => User can scroll if list is long
  
- **User taps "Steps" tab**
  - => View switches to numbered cooking instructions
  - => Each step displays clear, concise directions:
    - Step 1: "Preheat oven to 425°F (220°C). Pat the chicken dry with paper towels."
    - Step 2: "Stuff the chicken cavity with lemon halves and rosemary sprigs."
    - Step 3: "Rub the outside of the chicken with olive oil..."
  - => Instructions include specific temperatures and timing details
  
- **User taps back arrow (top left)**
  - => Returns to Chat screen
  - => Chat history preserved showing previous conversation and recipe card
  - => User can ask for another recipe or continue conversation
  
- **User asks follow-up question: "Something quicker?"**
  - => AI responds: "How about this 30-minute option?"
  - => New recipe card appears with faster recipe
  - => User can tap "View Recipe" to see new recipe details

**Additional Interactions:**

- **User scrolls through recipe steps while cooking**
  - => Steps remain clearly visible and readable
  - => User can switch back to Ingredients tab to check quantities
  
- **User receives another recipe suggestion in chat**
  - => Multiple recipe cards can appear in conversation
  - => Each has its own "View Recipe" button
  - => User can view any recipe from the chat history

## Wireframes

<img src="https://github.com/xlz1047/CookingMate/blob/master/Recipe%20Detail%20Screen%202.png" width=400>
<img src="https://github.com/xlz1047/CookingMate/blob/master/Recipe%20Detail%20Screen%201.png" width=400>
<img src="https://github.com/xlz1047/CookingMate/blob/master/Chat%20Screen.png" width=400>

*Wireframe includes:*
- **Screen 1**: Chat interface with AI conversation bubbles and recipe preview cards
- **Screen 2**: Recipe Detail screen with hero image, metadata, and ingredient/steps tabs

### [BONUS] Digital Wireframes & Mockups

*High-fidelity mockups showing:*
- Orange header (#F5A442) with app title
- Cream background (#F5E6D3) for warm cooking atmosphere
- Teal accents (#2D8B8A) for buttons and active states
- Chat bubbles: AI (white background) vs User (teal background)
- Recipe cards with rounded corners and drop shadows
- Large, appetizing food photography
- Clean typography with clear hierarchy
- Icon-based metadata display

### [BONUS] Interactive Prototype

## Build Notes

### Technical Architecture
- **Language:** Kotlin
- **Architecture:** MVVM (Model-View-ViewModel)
- **UI:** Jetpack Compose for modern Android UI
- **Database:** Room for local recipe storage
- **Networking:** Retrofit for API calls
- **Image Loading:** Coil for efficient image handling
- **Dependency Injection:** Hilt for clean dependency management

### Technical Architecture
- **Language:** Kotlin
- **Architecture:** MVVM (Model-View-ViewModel)
- **UI:** Jetpack Compose for modern Android UI
- **Navigation:** Jetpack Navigation Compose for screen transitions
- **Networking:** Retrofit for API calls
- **Image Loading:** Coil for efficient image handling
- **JSON Parsing:** Moshi or Gson for API response parsing
- **Async Operations:** Kotlin Coroutines for AI and recipe API calls

### Learning Goals
- Master Jetpack Compose for modern UI development
- Learn API integration with AI and recipe services
- Implement clean MVVM architecture
- Practice navigation between screens with data passing
- Develop conversational AI integration skills

For Milestone 2, include **2+ Videos/GIFs** of the build process here!

## License

Copyright 2025 CookingMate Team

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
