# **CookingMate**

## Table of Contents

1. [App Overview](#App-Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
1. [Build Notes](#Build-Notes)

## App Overview

### Description 

CookingMate is an AI-powered recipe assistant that helps users discover personalized recipes through natural conversation and organize them in a personal recipe book. Users chat with an AI to find recipes based on available ingredients, dietary preferences, or meal ideas, then save their favorites to a searchable recipe collection with detailed ingredients and cooking instructions.

### App Evaluation

- **Category:** Food & Drink / Lifestyle
- **Mobile:** Mobile is essential for accessing the AI chatbot and recipes while actively cooking in the kitchen. Users get real-time recipe suggestions through conversational interaction. The app provides on-the-go access to saved recipes when grocery shopping or planning meals away from home.
- **Story:** Eliminates the daily "What should I cook?" decision fatigue by making recipe discovery conversational and personalized. Instead of endless scrolling through recipe websites, users simply ask the AI and get immediate suggestions. Creates a personal recipe collection that grows over time with tried-and-true favorites.
- **Market:** Anyone who cooks at home could utilize this app - approximately 70% of adults cook regularly. Appeals to busy professionals needing quick dinner ideas, college students learning to cook, and home cooks looking to organize their recipes. Freemium model with premium features could be used for monetization.
- **Habit:** Users interact with the chatbot multiple times per week when planning meals. Daily use during active cooking periods when deciding what to make. Users constantly build and reference their recipe book, making it a regular kitchen companion.
- **Scope:** V1 allows users to chat with AI for recipe suggestions and view recipe details with ingredients and steps. Could be tested with real users cooking meals. V2 adds ability to save recipes to personal recipe book with search functionality. V3 incorporates filtering and sorting options for saved recipes. V4 adds serving size adjustment and recipe sharing features.

## Product Spec

### 1. User Features (Required and Optional)

Required Features:

- **AI Chatbot Interface** - Users can type natural language queries to discover recipes
- **Recipe Suggestions** - AI responds with personalized recipe recommendations based on queries
- **Recipe Preview Cards** - Visual recipe cards displayed in chat with images, time, and difficulty
- **View Recipe Details** - Tap recipe card to see full ingredients and step-by-step instructions
- **Save Recipes** - Bookmark recipes from detail view to personal recipe book
- **Recipe Book Grid** - Visual library displaying all saved recipes with images
- **Search Saved Recipes** - Search through saved recipes by name or ingredient
- **Ingredient Checklist** - Interactive checkboxes to mark off ingredients while cooking (TBD)
- **Cooking Steps** - Numbered step-by-step instructions with tab navigation

Stretch Features:

- **Voice Input** - Speak queries instead of typing for hands-free interaction
- **Camera Integration** - Take photos of ingredients for AI identification
- **Filter Recipes** - Filter by meal type, dietary restrictions, cooking time, difficulty
- **Sort Options** - Sort recipes by newest, alphabetical, or cooking time
- **Serving Adjustment** - Scale recipe ingredients based on number of servings
- **Share Recipes** - Share recipe details with friends via text/social media
- **Dark/Light Mode Toggle** - Switch between dark and light theme
- **Recipe Collections** - Organize saved recipes into custom folders/categories
- **Cooking Timer Integration** - Built-in timers for cooking steps
- **Offline Mode** - Access saved recipes without internet connection

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
  - => App launches to AI Chat screen with welcome message
  - => Bottom navigation shows Chat and Recipe Book tabs
  
- **User types "What can I make with chicken and rice?"**
  - => AI processes query and displays thinking indicator
  - => AI responds with conversational text and recipe suggestion
  - => Recipe card appears with image, title, time, and "View Recipe" button
  
- **User taps "View Recipe" on recipe card**
  - => App navigates to Recipe Detail screen
  - => Displays hero image, recipe title, time, servings, difficulty
  - => Shows Ingredients tab by default with checkboxes
  
- **User taps "Steps" tab**
  - => View switches to numbered cooking instructions
  - => Each step displays clear, concise directions
  
- **User taps bookmark/save icon**
  - => Recipe is added to Recipe Book
  - => Visual confirmation (toast/snackbar message)
  - => Bookmark icon fills in to show saved state
  
- **User navigates to Recipe Book tab**
  - => Displays grid of saved recipe cards with images
  - => Shows recipe name, time, and difficulty on each card
  - => If empty, shows "No Saved Recipes Yet" with explore button
  
- **User taps search icon in Recipe Book**
  - => Search bar appears at top of screen
  - => User types recipe name or ingredient
  - => Recipe grid filters in real-time to show matches
  
- **User taps a saved recipe card**
  - => Opens Recipe Detail screen for that recipe
  - => User can review ingredients and steps
  - => User can unsave recipe if desired
  
- **User checks off ingredients while shopping**
  - => Checkbox marks ingredient as obtained
  - => Visual strikethrough or color change indicates completion
  - => Progress persists if user leaves and returns

## Wireframes

<img src="https://i.imgur.com/your-wireframe-url.png" width=600>

*Wireframe includes:*
- Chat Screen with AI conversation and recipe cards
- Recipe Book Screen with grid layout of saved recipes
- Recipe Detail Screen with ingredients, steps, and actions

### [BONUS] Digital Wireframes & Mockups

<img src="https://i.imgur.com/your-mockup-url.png" width=600>

*High-fidelity mockups showing:*
- ___ theme with ___ accents
- Chat interface with bubble messages
- Recipe cards with food photography
- Recipe detail layout with tabs

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

### Key Challenges
- Integrating AI API efficiently within mobile constraints
- Designing intuitive chat interface with embedded recipe cards
- Managing recipe data persistence and sync
- Optimizing image loading for smooth scrolling
- Implementing real-time search filtering

### Learning Goals
- Master Jetpack Compose for modern UI development
- Learn API integration with multiple services
- Implement clean MVVM architecture
- Practice Room database operations
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
