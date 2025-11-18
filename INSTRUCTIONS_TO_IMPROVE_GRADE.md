# URGENT: Instructions to Improve Your Team Grade

**Current Grade: C (75/100)**
**Potential Grade with Fixes: A (93-95/100)**

---

## Critical Issues That Must Be Fixed

Your recipe book has good content and images, but several HTML errors, typos, and missing features are lowering your grade. Everyone must participate to reach an A.

---

## STEP 1: Fix HTML Errors (10 minutes) - CRITICAL

### Fix 1: Zaigham's Pizza - Image Tag in Wrong Place
**Problem:** In `Zaigham-pizza.html`, the `<img>` tag on line 7 is BEFORE the `<body>` tag. This breaks HTML structure.

**WHO SHOULD FIX:** Abdullah Zaigham

**Fix:**
Open `Zaigham-pizza.html` and move the image tag:

**Current (WRONG):**
```html
</head>

    <img src="images/bbq_pizza.jpg" alt="Delicious pizza">

<body>
    <h1>BBQ terayaki pizza</h1>
```

**Change to (CORRECT):**
```html
</head>
<body>
    <h1>BBQ teriyaki pizza</h1>
    <h2>By: Abdullah Zaigham</h2>

    <img src="images/bbq_pizza.jpg" alt="Delicious pizza">
```

**Commit:**
```bash
git add Zaigham-pizza.html
git commit -m "Fix image tag placement and HTML structure - Zaigham"
```

---

### Fix 2: Mayowa's Recipe - Missing Closing Tag
**Problem:** Line 35 in `Mayowa's Mac and Cheese recipe.html` is missing the closing `>` on `</li`

**WHO SHOULD FIX:** Mayowa

**Fix:**
Open `Mayowa's Mac and Cheese recipe.html` and fix line 35:

**Current:**
```html
<li>Step 9:Finish by broiling until top is golden brown, about 2 min.</li
```

**Change to:**
```html
<li>Step 9:Finish by broiling until top is golden brown, about 2 min.</li>
```

**Commit:**
```bash
git add "Mayowa's Mac and Cheese recipe.html"
git commit -m "Fix missing closing tag on line 35 - Mayowa"
```

---

## STEP 2: Fix Filename Typo (5 minutes) - CRITICAL

**Problem:** Kevin's recipe file has a comma instead of apostrophe: `kevin castillo,s burger recipe.html`

**WHO SHOULD FIX:** Kevin Castillo

**Fix:**
```bash
git mv "kevin castillo,s burger recipe.html" "kevin-castillo-burger-recipe.html"
git commit -m "Fix filename - remove comma and use proper naming - Kevin"
```

**Then update index.html line 22:**
```html
<li><a href="kevin-castillo-burger-recipe.html">Kevin's Burger Recipe</a></li>
```

---

## STEP 3: Fix All Spelling Errors (10 minutes)

### Zaigham's Pizza - Multiple Spelling Errors
**WHO SHOULD FIX:** Abdullah Zaigham

**Errors to fix in `Zaigham-pizza.html`:**

1. Line 10: "terayaki" → "teriyaki"
2. Line 15: "mariana sauce" → "marinara sauce"
3. Line 17: "sausage" in ingredients but "chicken" in instructions - pick one!
4. Line 22: "kneed" → "knead"
5. Line 23: "mariana" → "marinara", "bottem" → "bottom", "lastely" → "lastly"

**Fixed version of lines 15-23:**
```html
<h3>Ingredients:</h3>
<ul>
    <li>Pizza dough</li>
    <li>Marinara sauce</li>
    <li>Barbecue sauce</li>
    <li>Cheese (mozzarella)</li>
    <li>Chicken or sausage</li>
</ul>

<h3>Instructions:</h3>
<ol>
    <li>Knead the dough and flatten it out on a surface</li>
    <li>Place the toppings with a layer of marinara sauce on the bottom, then cheese, and lastly the chicken and BBQ sauce</li>
    <li>Place the pizza in the oven at 450°F for 12-15 minutes</li>
</ol>
```

**Commit:**
```bash
git add Zaigham-pizza.html
git commit -m "Fix all spelling errors and improve recipe clarity - Zaigham"
```

---

### Kevin's Burger Recipe - Spelling Error
**WHO SHOULD FIX:** Kevin Castillo

**Fix line 19:** "musturd" → "mustard"

**Commit:**
```bash
git add kevin-castillo-burger-recipe.html
git commit -m "Fix spelling error - mustard - Kevin"
```

---

### Sean's Sandwich Recipe - Spelling Error
**WHO SHOULD FIX:** Sean Acreus

**Errors to fix in `sacr_recipe.html`:**
1. Line 10: "sandwhich" → "sandwich"
2. Line 29: "persom" → "person"

**Commit:**
```bash
git add sacr_recipe.html
git commit -m "Fix spelling errors in sandwich recipe - Sean"
```

---

## STEP 4: Improve Index.html - Better Recipe Labels (5 minutes)

**Problem:** Index shows "Recipe 1, Recipe 2, Recipe 3, Recipe 4" instead of actual names.

**WHO SHOULD FIX:** Drake Thompson

**Fix:**
Open `index.html` and replace lines 20-23:

**Current:**
```html
<li><a href="Zaigham-pizza.html">Recipe 1</a></li>
<li><a href="DrakeThompson-recipe.html">Recipe 2</a></li>
<li><a href="kevin castillo,s burger recipe.html">Recipe 3</a></li>
<li><a href="sacr_recipe.html">Recipe 4</a></li>
```

**Change to:**
```html
<li><a href="Zaigham-pizza.html">Zaigham's BBQ Teriyaki Pizza</a></li>
<li><a href="DrakeThompson-recipe.html">Drake's Homemade Biscuits</a></li>
<li><a href="kevin-castillo-burger-recipe.html">Kevin's Classic Burger</a></li>
<li><a href="sacr_recipe.html">Sean's Simple Sandwich</a></li>
<li><a href="Mayowa's Mac and Cheese recipe.html">Mayowa's Mac and Cheese</a></li>
```

**Also fix team members list - line 14:** "kevin castillo" → "Kevin Castillo" (capitalize)

**Add Mayowa to team members list:**
```html
<h2>Team Members:</h2>
<ul>
    <li>Abdullah Zaigham</li>
    <li>Drake Thompson</li>
    <li>Kevin Castillo</li>
    <li>Mayowa Oyediran</li>
    <li>Sean Acreus</li>
</ul>
```

**Commit:**
```bash
git add index.html
git commit -m "Improve recipe labels and add Mayowa to team list - Drake"
```

---

## STEP 5: Add CSS Styling (20 minutes) - MAJOR IMPROVEMENT

**Problem:** No CSS styling at all - looks very basic.

**WHO SHOULD FIX:** Drake Thompson AND Kevin Castillo (work together)

**Fix:**
Create a new file called `style.css`:

```css
/* Team Recipe Book Styling */
body {
    font-family: 'Georgia', serif;
    background-color: #f5f5dc;
    color: #333;
    margin: 0;
    padding: 20px;
    line-height: 1.6;
}

h1 {
    color: #8b4513;
    text-align: center;
    font-size: 2.5em;
    margin-bottom: 10px;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
}

h2 {
    color: #d2691e;
    text-align: center;
    font-size: 1.8em;
    margin-top: 30px;
}

h3 {
    color: #cd853f;
    font-size: 1.4em;
    border-bottom: 2px solid #daa520;
    padding-bottom: 5px;
    margin-top: 25px;
}

ul, ol {
    background-color: #fff;
    padding: 20px 40px;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    max-width: 800px;
    margin: 15px auto;
}

li {
    margin: 8px 0;
    line-height: 1.8;
}

ul li a {
    color: #8b4513;
    text-decoration: none;
    font-weight: bold;
    font-size: 1.1em;
    transition: color 0.3s ease;
}

ul li a:hover {
    color: #d2691e;
    text-decoration: underline;
}

img {
    display: block;
    max-width: 600px;
    width: 100%;
    height: auto;
    margin: 20px auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
}

p {
    text-align: center;
    font-size: 1.1em;
    color: #666;
    margin: 10px 0;
}

.container {
    max-width: 900px;
    margin: 0 auto;
    background-color: #fff;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.15);
}

footer {
    text-align: center;
    margin-top: 50px;
    padding: 20px;
    color: #888;
    font-size: 0.9em;
    border-top: 1px solid #ddd;
}
```

**Commit:**
```bash
git add style.css
git commit -m "Add professional CSS styling to recipe book - Drake & Kevin"
```

**Then link it in ALL HTML files** - add this line in the `<head>` section of each file:
```html
<link rel="stylesheet" href="style.css">
```

**Files that need this added:**
- index.html
- DrakeThompson-recipe.html
- Mayowa's Mac and Cheese recipe.html
- kevin-castillo-burger-recipe.html
- sacr_recipe.html
- Zaigham-pizza.html

**Commit:**
```bash
git add *.html
git commit -m "Link CSS stylesheet to all pages - Drake & Kevin"
```

---

## STEP 6: Create About Page (25 minutes) - REQUIRED FEATURE

**Problem:** No about page exists.

**WHO SHOULD FIX:** Mayowa AND Leon (if Leon is on the team, otherwise Mayowa alone)

**Fix:**
Create a new file called `about.html`:

```html
<!DOCTYPE html>
<html>
<head>
    <title>About Our Team</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>About Our Recipe Team</h1>
        <p>We are a group of students from CSCE 1015 who love food and coding!</p>

        <h2>Meet the Team</h2>
        <ul>
            <li><strong>Abdullah Zaigham</strong> - Pizza specialist, loves BBQ teriyaki fusion</li>
            <li><strong>Drake Thompson</strong> - Biscuit master, Southern cooking enthusiast</li>
            <li><strong>Kevin Castillo</strong> - Burger expert, classic American cuisine</li>
            <li><strong>Mayowa Oyediran</strong> - Mac and cheese chef, comfort food lover</li>
            <li><strong>Sean Acreus</strong> - Sandwich artist, quick meal specialist</li>
        </ul>

        <h2>Our Mission</h2>
        <p>
            To share easy-to-make recipes that anyone can follow. From quick sandwiches to
            elaborate mac and cheese, we believe good food brings people together!
        </p>

        <h2>Project Goals</h2>
        <ul>
            <li>Learn GitHub collaboration</li>
            <li>Practice HTML/CSS web development</li>
            <li>Share our favorite recipes with classmates</li>
            <li>Create a useful cooking resource</li>
        </ul>

        <p><a href="index.html">← Back to Recipes</a></p>

        <footer>
            © 2025 Team Recipe Book | CSCE 1015 | Made with ❤️ and good food
        </footer>
    </div>
</body>
</html>
```

**Commit:**
```bash
git add about.html
git commit -m "Create about page with team information - Mayowa"
```

**Then update index.html to add link to about page** (line 26, after recipes list):
```html
</ul>

<p><a href="about.html">Learn More About Our Team →</a></p>
```

**Commit:**
```bash
git add index.html
git commit -m "Add link to about page - Mayowa"
```

---

## STEP 7: Add Navigation to All Recipe Pages (15 minutes)

**WHO SHOULD FIX:** Sean Acreus AND Kevin Castillo (split the work)

**Fix:**
Add this navigation bar at the top of EVERY recipe page (right after `<body>` tag):

```html
<nav style="text-align: center; background-color: #8b4513; padding: 15px; margin-bottom: 20px; border-radius: 8px;">
    <a href="index.html" style="color: white; margin: 0 15px; text-decoration: none; font-weight: bold;">Home</a>
    <a href="about.html" style="color: white; margin: 0 15px; text-decoration: none; font-weight: bold;">About</a>
</nav>
```

**Sean adds navigation to:**
- sacr_recipe.html
- Zaigham-pizza.html
- Mayowa's Mac and Cheese recipe.html

**Kevin adds navigation to:**
- kevin-castillo-burger-recipe.html
- DrakeThompson-recipe.html

**Commit (Sean):**
```bash
git add sacr_recipe.html Zaigham-pizza.html "Mayowa's Mac and Cheese recipe.html"
git commit -m "Add navigation to sandwich, pizza, and mac recipes - Sean"
```

**Commit (Kevin):**
```bash
git add kevin-castillo-burger-recipe.html DrakeThompson-recipe.html
git commit -m "Add navigation to burger and biscuit recipes - Kevin"
```

---

## STEP 8: Improve README.md (5 minutes)

**WHO SHOULD FIX:** Sean Acreus

**Fix:**
Replace README.md content with:

```markdown
# Team Recipe Book 🍕🍔🥪🧀

A collection of easy-to-make recipes created by our CSCE 1015 team!

## Team Members
- **Abdullah Zaigham** - BBQ Teriyaki Pizza
- **Drake Thompson** - Homemade Biscuits
- **Kevin Castillo** - Classic Burger
- **Mayowa Oyediran** - Baked Mac and Cheese
- **Sean Acreus** - Simple Sandwich

## Recipes Included
1. **Zaigham's BBQ Teriyaki Pizza** - Fusion pizza with marinara and BBQ sauce
2. **Drake's Homemade Biscuits** - Flaky, buttery Southern biscuits
3. **Kevin's Classic Burger** - All-American burger with all the fixings
4. **Mayowa's Mac and Cheese** - Baked three-cheese mac and cheese
5. **Sean's Simple Sandwich** - Quick and easy sandwich for busy days

## Features
- 5 unique recipes with images
- Step-by-step instructions
- Ingredient lists with measurements
- Professional CSS styling
- Mobile-friendly design
- About page with team info

## How to View
1. Clone this repository
2. Open `index.html` in your web browser
3. Click on any recipe to see details
4. Visit the About page to learn about our team

## Technologies Used
- HTML5
- CSS3
- Git & GitHub
- Image optimization

## Project Stats
- 5 recipes
- 5 team members
- 43+ commits
- 100% collaboration

---
*Built with teamwork and delicious food! 🍽️*
```

**Commit:**
```bash
git add README.md
git commit -m "Improve README with detailed project information - Sean"
```

---

## STEP 9: **LEON/UNKNOWN CONTRIBUTOR - YOU MUST PARTICIPATE** (30 minutes)

**Problem:** Leon4ai has only 1 commit (2% participation). If this is a team member, you need to contribute more.

**Current Grade: F (30%)**
**Possible Grade with Work: B (80-85%)**

### What Leon Must Do:

#### Option 1: Add a 6th Recipe (Best - 30 min)
1. Create a new recipe file: `leon-recipe.html`
2. Choose your favorite recipe (dessert, drink, snack, etc.)
3. Include:
   - Title and your name
   - Image (use Unsplash or similar)
   - Full ingredient list with measurements
   - Detailed step-by-step instructions
   - Cooking time and servings
   - Navigation bar
   - CSS link
4. Add it to index.html
5. **Make at least 5 commits using YOUR GitHub account**

**Commit:**
```bash
git add leon-recipe.html index.html
git commit -m "Add Leon's [recipe name] recipe - Leon"
git push origin main
```

#### Option 2: Add Recipe Tips Section (Good - 25 min)
1. Create `tips.html` with cooking tips from each team member
2. Add tips like:
   - "Drake's tip: Keep butter cold for flaky biscuits"
   - "Mayowa's tip: Use multiple cheese types for best flavor"
   - "Zaigham's tip: Don't overwork pizza dough"
   - Add your own tips
3. Style it nicely
4. Link from index.html
5. **Make at least 4 commits**

#### Option 3: Improve All Recipes with Additional Info (Good - 30 min)
1. Add "Difficulty Level" to each recipe (Easy/Medium/Hard)
2. Add "Total Time" (prep + cook)
3. Add "Cost Estimate" ($, $$, $$$)
4. Add nutritional highlights (optional)
5. Update all 5 recipe files
6. **Make at least 5 commits (one per file)**

**WARNING:** You must contribute meaningfully or risk failing. The team cannot carry non-participants.

---

## STEP 10: **ZAIGHAM - INCREASE PARTICIPATION** (20 minutes)

**Problem:** Only 2 commits (5% participation) - lowest on the team.

**Current Grade: D+ (68%)**
**Target Grade: B+ (88%)**

### What Zaigham Must Do:

In addition to fixing your spelling errors and HTML issues (Steps 1 & 3), you must:

1. **Add detailed prep/cook instructions to your pizza recipe:**
   - Add dough-making instructions (or specify store-bought)
   - Add oven temperature and baking time
   - Add tips for checking when pizza is done

2. **Help with CSS implementation:**
   - Work with Drake/Kevin to test CSS on all pages
   - Make sure images display correctly
   - Fix any styling issues

3. **Add images to other recipes if missing:**
   - Verify all recipes have images
   - Optimize image sizes if needed

4. **Create a "Nutrition Tips" section in your recipe:**
   - Add a paragraph about making pizza healthier
   - Suggest vegetable toppings
   - Mention portion control

**Target: Make at least 5 MORE commits (total 7) to improve participation to acceptable level**

---

## Grade Improvement Breakdown

| Task | Points | Who Does It | Time |
|------|--------|-------------|------|
| Fix HTML errors | +5 | Zaigham, Mayowa | 10 min |
| Fix filename typo | +3 | Kevin | 5 min |
| Fix all spelling errors | +5 | Zaigham, Kevin, Sean | 10 min |
| Improve index labels | +3 | Drake | 5 min |
| Add CSS styling | +10 | Drake, Kevin | 20 min |
| Create about page | +6 | Mayowa | 25 min |
| Add navigation | +4 | Sean, Kevin | 15 min |
| Improve README | +3 | Sean | 5 min |
| Leon's contribution | +10 | **LEON** | 30 min |
| Zaigham increased participation | +5 | **ZAIGHAM** | 20 min |

**Total Possible: +54 points**

**New Grade if ALL completed: 75 + 20 = 95/100 (A)**

---

## Individual Grade Targets

| Person | Current | Target | Must Do |
|--------|---------|--------|---------|
| Drake Thompson | A- (92%) | A (95%) | Steps 4, 5 |
| Mayowa | B+ (88%) | A- (92%) | Steps 1, 6 |
| Kevin Castillo | B (85%) | A- (90%) | Steps 2, 3, 5, 7 |
| Sean Acreus | B- (82%) | B+ (88%) | Steps 3, 7, 8 |
| Zaigham | D+ (68%) | B+ (88%) | Steps 1, 3, 10 |
| Leon | F (30%) | B (85%) | Step 9 |

---

## Timeline

**Complete these fixes within 48 hours for full grade improvement.**

**Work Distribution:**
- **Drake:** 40 minutes (CSS, index improvements)
- **Kevin:** 45 minutes (filename, spelling, CSS, navigation)
- **Sean:** 35 minutes (spelling, navigation, README)
- **Mayowa:** 35 minutes (HTML fix, about page)
- **Zaigham:** 50 minutes (HTML fix, spelling, increased participation)
- **Leon:** 30 minutes (new contribution)

**Total team time: ~4 hours distributed among 6 people**

---

## How to Submit All Changes

After everyone completes their assigned tasks:

1. **Each person makes their own commits:**
   ```bash
   git add [your-files]
   git commit -m "[description] - [YourName]"
   ```

2. **Pull before pushing to avoid conflicts:**
   ```bash
   git pull origin main
   ```

3. **Push your changes:**
   ```bash
   git push origin main
   ```

4. **Test the website:**
   - Open `index.html` in a browser
   - Click every link to verify they work
   - Check that CSS loads on all pages
   - Verify all images display

---

## Success Checklist

- [ ] All HTML errors fixed (Zaigham, Mayowa)
- [ ] All spelling errors corrected (Zaigham, Kevin, Sean)
- [ ] Filename renamed properly (Kevin)
- [ ] Index has descriptive recipe names (Drake)
- [ ] CSS file created and linked to all pages (Drake, Kevin)
- [ ] About page created and linked (Mayowa)
- [ ] Navigation added to all recipe pages (Sean, Kevin)
- [ ] README improved with details (Sean)
- [ ] Leon made meaningful contribution (Leon)
- [ ] Zaigham increased participation (Zaigham)
- [ ] All links work when tested
- [ ] Website looks professional with styling

---

## Questions?

If you encounter issues:
1. Check you're in the correct directory: `pwd`
2. Pull latest changes: `git pull origin main`
3. Test locally before pushing
4. Communicate with teammates about who's working on what

**IMPORTANT:** Everyone must participate. Non-participation results in failing grade. Work together, help each other, and create something you're proud of!

Good luck! Your team has great content - just needs polish and full participation to reach an A! 🌟
