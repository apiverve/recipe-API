Recipes API
============

Recipes is a simple tool for getting recipe information. It returns information on various recipes.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)

This is a Javascript Wrapper for the [Recipes API](https://apiverve.com/marketplace/api/recipe)

---

## Installation
	npm install @apiverve/recipe --save

---

## Configuration

Before using the recipe API client, you have to setup your account and obtain your API Key.  
You can get it by signing up at [https://apiverve.com](https://apiverve.com)

---

## Usage

The Recipes API documentation is found here: [https://docs.apiverve.com/api/recipe](https://docs.apiverve.com/api/recipe).  
You can find parameters, example responses, and status codes documented here.

### Setup

```
var recipeAPI = require('@apiverve/recipe');
var api = new recipeAPI({
    api_key: [YOUR_API_KEY],
    secure: true //(Optional, defaults to true)
});
```

---


### Perform Request
Using the API client, you can perform requests to the API.

###### Define Query

```
var query = {
  name: "chicken"
};
```

###### Simple Request (using Callback)

```
api.execute(query, function (error, data) {
    if (error) {
        return console.error(error);
    } else {
        console.log(data);
    }
});
```

###### Example Response

```
{
  "status": "ok",
  "error": null,
  "data": {
    "count": 10,
    "recipes": [
      {
        "instructions": "Heat the oil in a large, non-stick frying pan or wok and stir-fry the chicken and peppers for 2 mins. Sprinkle over the spices and cook for 30 secs more, stirring. Tip the tomatoes into the pan and stir in the chipotle paste. Simmer for 5 mins or until the sauce is thick and glossy, stirring regularly. Stir in the spring onions and coriander, cook for 1 min more, then remove from the heat and leave to cool. Cut the tortillas into quarters, then cut each quarter into three pieces, so you have 36 triangles. Place 1 tsp of the chicken mixture and a little cheese at the widest end of a triangle. Roll the pointed end of the triangle around the filling and secure with a cocktail stick. Place on a baking tray lined with baking parchment. Fill and roll the other triangles. Cover with cling film and chill for up to 8 hrs until ready to reheat. To make the dip, mash all the ingredients in a bowl until almost smooth. Cover the surface of the dip with cling film and chill for up to 24 hrs. When ready to serve, heat oven to 200C/180C fan/gas 6. Uncover the fajitas and bake for 6-8 mins or until hot throughout. Serve with the guacamole.",
        "name": "Mini Chicken Fajitas",
        "ingredients": [
          "2 tbsp sunflower oil",
          "2 skinless chicken breasts, cut into 1½ cm/½ in chunks",
          "1 red pepper, deseeded and cut into 1½ cm/½ in chunks",
          "1 yellow pepper, deseeded and cut into 1½ cm/½ in chunks",
          "1 tsp ground cumin",
          "1 tsp ground coriander",
          "¼ tsp hot chilli powder",
          "227g can chopped tomatoes",
          "2 tbsp chipotle paste",
          "4 spring onions, trimmed and thinly sliced",
          "large pack coriander, leaves chopped",
          "3 large flour tortillas",
          "75g ready-grated mozzarella",
          "1 ripe avocado, stoned and peeled",
          "juice 1 large lime",
          "1 garlic clove, crushed",
          "2 heaped tbsp finely chopped coriander",
          "36 cocktail sticks"
        ]
      },
      {
        "instructions": "Put the chicken in a large pot. Halve 1 onion, 1 celery stick and 1 carrot. Add to the pot with the herbs, peppercorns and a sprinkling of salt. Add water to come halfway up the chicken, bring to the boil, then cover tightly and simmer for 1½ hrs. Cool slightly, remove the chicken to a dish, then strain the stock into a bowl. When the chicken is cool enough to handle, strip the meat from the bones and tear into pieces with your hands. Chop the remaining onion, and cut the celery and carrots into thick slices. Heat the butter in the same pot, add the onion and lardons, then gently fry for 5 mins until just starting to brown. Add the remaining veg, then fry for 2 mins. Stir in the flour, then cook for 1 min. Measure 900ml stock (if you don’t have enough, make it up with water), then gradually add to the pan, stirring. Cover, then simmer for 20-25 mins until vegetables are tender. Return the chicken to the pan with the mustard and crème fraîche, then return to a simmer, stirring gently. Season and sprinkle with parsley.",
        "name": "Mustard Chicken With Winter Vegetables",
        "ingredients": [
          "1 chicken, about 1.8kg/4lb in weight",
          "2 onions",
          "6 celerysticks",
          "6 carrots",
          "2 bay leaves",
          "2 thymesprigs",
          "1 tsp black peppercorn",
          "50g butter",
          "100g smoked baconlardons",
          "3 small turnips, peeled and cut into wedges",
          "1 tbsp plain flour",
          "2 tbsp wholegrain mustard",
          "3 rounded tbsp crème fraîche",
          "good handful parsley, chopped"
        ]
      },
      {
        "instructions": "Heat 1 tbsp of the coconut oil in a large flameproof casserole dish over a medium heat. When melted and hot, add the onion, pepper and garlic. Cook, stirring regularly, for 3 -4 mins or until just starting to soften. Increase the heat to maximum and add the chicken thighs. Fry everything together for about 3 mins, stirring occasionally. Sprinkle in the spices, squeeze in the tomato purée and fry, stirring almost constantly, for 1 min. Pour in the stock and bring to the boil. Reduce the heat to a simmer and partially cover with a lid. After 30 mins, add the dried apricots and chickpeas, and continue to simmer for a further 10 mins. While the tagine is bubbling away, heat the remaining 1/ 2 tbsp of coconut oil in a frying pan over a high heat. When melted, add the cumin seeds, toast for 10 secs, then add the shredded sprouts. Fry the sprouts over the high heat, stirring almost constantly, for 5 mins, by which time they should have softened and browned in places. Serve the tagine in a large bowl, scatter over the fried sprouts, crumble over the feta and finish with the coriander.",
        "name": "Chicken Tagine With Spiced Brussels Sprouts & Feta",
        "ingredients": [
          "1 ½ tbsp coconut oil",
          "1 large red onion, sliced",
          "1 red pepper, finely sliced",
          "3 garlic cloves, finely chopped",
          "10 chicken thighsfillets (boneless and skinless)",
          "½ tsp ground cinnamon",
          "½ tsp ground turmeric",
          "½ tsp smoked paprika",
          "1 tbsp tomato purée",
          "250ml chicken stock",
          "6 dried apricots, cut in half",
          "175g canned chickpeas, drained and rinsed",
          "½ tsp cumin seeds",
          "275g Brussels sprouts, shredded",
          "50g feta",
          "½ small bunch coriander, roughly chopped"
        ]
      },
      {
        "instructions": "Soften the onion in the butter with the sage and mace. Cool for a few mins while you whizz the chicken thighs and 300g of the ham in a food processor until minced. Scrape into a large bowl and stir in the softened onion, pistachios, cranberries, apricots and parsley. Season with nutmeg, lots of black pepper and some salt. Grease a deep, 20cm round springform or loose-bottomed tin, then line with baking parchment. To make the pastry, mix together the flours and 2 tsp salt in a large bowl, then make a well in the centre. Put the butter and lard into a small pan with 200ml water and very gently melt. Once melted, turn up the heat and when just bubbling, pour into the well and stir with a wooden spoon to a dough – don’t worry if some powdery bits remain. Once cool enough to handle, knead in the bowl until the dough comes together, then tip onto your work surface. Set aside a third, wrapped in a clean tea towel to keep it as warm and pliable as possible, while you quickly roll the remaining dough into a large circle – big enough to line the tin with a little overhanging. Ease the circle into the tin, pressing evenly into the corners and side – you can be rough with it. Evenly cover the base with half the remaining sliced ham, followed by half the chicken breasts and half the mince mixture, pressing firmly to pack. Repeat with the remaining ham and chicken, then a rounded dome of mince. Put a pie funnel, if you have one, on the top. Roll the reserved dough to a circle large enough to easily cover the pie, cutting out a hole (if using a pie funnel). Brush the edge of the pie with some beaten egg and top with the pastry lid. Press to seal the edges before trimming the excess. Crimp the edges between your thumb and forefinger to seal thoroughly, then make a small hole in the middle to let steam escape (if not using a pie funnel). Brush the top of the pie with more beaten egg. Heat oven to 200C/180 fan/gas 6. Bake the pie for 1 hr. Very, very carefully remove the pie from its tin, brush the top and side with more egg and bake for another 30 mins until browned and crisp. Leave to cool completely before chilling. To make the jelly, soak the gelatine in cold water for 5-10 mins until soft. Squeeze out any excess water from the gelatine, then dissolve in the hot stock. Once cooled, carefully pour into your chilled pie through the small hole, using a funnel, until full – you may not need all the stock. Chill the pie for a few hrs. Serve with chutney and salad, if you like.",
        "name": "Four & Twenty Chicken & Ham Pie",
        "ingredients": [
          "1 large onion, chopped",
          "1 tbsp butter, plus extra for greasing",
          "1 tbsp chopped sage",
          "1 tsp ground mace",
          "300g boneless, skinless chicken thigh(about 3)",
          "1kg cooked ham, trimmed of fat and thickly sliced",
          "50g shelled pistachio",
          "50g cranberry(fresh or frozen)",
          "50g dried apricot, diced",
          "3 tbsp chopped parsley",
          "good grating nutmeg",
          "700g skinless chicken breast, halved to thin",
          "chutney and saladto serve, (optional)",
          "375g plain white flour",
          "375g strong white flour",
          "140g butter",
          "175g lard",
          "1 egg, beaten",
          "3 gelatine leaves",
          "500ml strong chicken stock, heated"
        ]
      },
      {
        "instructions": "Put the dried fruit and dessert wine in a bowl. Cover and microwave on High for 3 mins. Meanwhile, gently melt the butter in a large pan and fry the livers with the garlic, sage and plenty of black pepper for about 5 mins until browned. Tip the mixture into a food processor, scraping in all of the buttery juices and blend until smooth. Pour in the cream and 2 tbsp of the wine from the dried fruit, season with salt, then blend again. Generously oil the insides of 8 x 100ml ramekins. Spoon some wine-soaked raisins into the base of each ramekin, then top with the parfait. Cover and chill. They will keep for 2 days in the fridge or 1 month in the freezer. Thaw overnight in the fridge. To serve, run a knife round the inside of the ramekins and turn the parfait out onto plates. Accompany with toasted brioche and a few salad leaves.",
        "name": "Chicken Liver Parfait With Sultanas & Raisins",
        "ingredients": [
          "100g jumbo sultana and raisins",
          "6 tbsp sweet dessert wine",
          "100g unsalted butter",
          "2 x 400g/14oz packs chicken livers, cleaned",
          "2 garlic cloves, crushed",
          "2 tbsp chopped sage",
          "150ml pot double cream",
          "thinly sliced brioche rolls",
          "few salad leaves"
        ]
      },
      {
        "instructions": "To make the gratin, peel and slice the potatoes no thicker than a 50p piece using a mandolin, if you have one. Bring the milk, cream, garlic, herbs and some seasoning to the boil in a large saucepan, then turn down the heat and simmer for a few mins. Slip the potatoes into the hot milk mixture and simmer for 10 mins until just cooked. Drain the potatoes in a colander over a bowl to catch the liquid – reserve the milk. While the potatoes are simmering, heat half the butter in a frying pan until foaming. Fry the mushrooms for 2 mins until just wilted, season with salt and pepper and set aside. Rub 2 small gratin dishes (or 1 medium) with the remaining butter, sprinkle over the thyme leaves and grate over some of the cheese. Fill the dishes halfway with potato slices, moisten with a little milk and grate over more cheese. Fill up the dishes with potato slices, add enough milk to cover, then top with the mushrooms and the rest of the cheese. For the chicken, mix about two-thirds of the butter with the lemon zest and half the juice, the parsley, paprika and some salt and pepper. Lift the skin slightly away from each breast, spread or pipe the flavoured butter under the skin, then stretch the skin back over. Chill up to a day in advance, if you like. Heat oven to 220C/200C fan/gas 7. Heat the remaining butter in an ovenproof frying pan until foaming. Pan-fry the chicken, basting constantly with the butter until starting to brown. Add the shallot, garlic, thyme and stock. Place the chicken, skin-side up in its pan, on the higher shelf of the oven, and the gratins on the lower shelf. Roast both for 25-30 mins, then remove the chicken and rest for 15 mins, while the gratins continue to cook. To finish, remove the chicken from the pan. Place the pan back on the heat, squeeze over the remaining lemon juice and bring everything to a hard boil. Pass the sauce through a sieve, pressing down firmly on all the soft shallot and garlic. Heat a drizzle of olive oil in another frying pan and reheat the leeks until they start to colour. With the gratins cooked, you are now ready to plate up. Line six leeks up in a row in the middle of each plate. Carve the chicken on a slant into five thick slices. Neatly fan out each chicken breast over the leeks. Spoon the sauce over the chicken and around the leeks, and serve with the potato gratin.",
        "name": "Butter-Roasted Supreme Of Chicken With Wild Mushroom & Potato Gratin",
        "ingredients": [
          "600g potatoes, preferably Maris Piper",
          "350ml full-fat milk",
          "350ml double cream",
          "1 large garlic clove, smashed",
          "1 bay leaf",
          "thymesprigs, plus a few extra thyme leaves for sprinkling",
          "50g butter",
          "300g mixed wild mushrooms, cleaned and roughly sliced if large",
          "50g Comté or gruyèrecheese",
          "200g softened butter",
          "zest and juice 1 lemon",
          "bunch flat-leaf parsley, leaves very roughly chopped",
          "large pinch paprika",
          "4 large chicken breasts, preferably supremes with the wing bone still attached",
          "1 large shallot, sliced",
          "1 garlicbulb, roughly chopped",
          "3 thymesprigs",
          "200ml fresh chicken stock",
          "1 tbsp olive oil",
          "24 baby leeks, trimmed to the same size, boiled for 3 mins, then refreshed in iced water"
        ]
      },
      {
        "instructions": "Heat oven to 190C/170C fan/gas 5. Heat the oil in a large frying pan, then soften the onions for 10 mins with the pan covered. Turn up the heat, add the mushrooms and fry for about 10 mins until golden and all their liquid has evaporated. Stir in the garlic and cook for 1 min more. Tip everything onto a plate. Pat the livers dry, then add a little more oil to the pan. Sizzle in batches for about 20 secs on each side until just golden but not cooked through. Set aside on a plate as you go. Tip in the brandy and let it reduce to 1 tbsp. Roughly chop the livers once cooled, then mix with the oniony mushrooms, brandy, bread and almost all the parsley and nuts. To cook, wind bacon rashers into the wells of a 12-hole bun tin, like little nests. Spoon in the stuffing (reserving 250g for your turkey), scatter with remaining nuts, then bake, covered with foil, for 20 mins. Uncover and cook for 25 mins more until the bacon is gold. Scatter with remaining chopped parsley to serve.",
        "name": "Chicken Liver & Mushroom Nests",
        "ingredients": [
          "3 tbsp sunflower oil",
          "3 onions, finely chopped",
          "250g pack chestnut mushroom, chopped",
          "1 garlic clove, crushed",
          "400g pack chicken liver, trimmed of any sinewy bits",
          "3 tbsp brandy",
          "140g white breadcrumb",
          "bunch flatleaf parsley, chopped",
          "handful walnuts, chopped",
          "12 smoked, dry-cured streaky bacon rashers"
        ]
      },
      {
        "instructions": "At least an hour before you want to make the tart, make the pastry. Tip the flour, thyme, butter and ½ tsp salt into a food processor and pulse to the texture of breadcrumbs. Add the egg yolk and milk and pulse again until it all starts to come together. Tip out and press into a ball of pastry. Wrap, then chill for at least 1 hr. Can be prepared up to 2 days ahead. On a lightly floured surface, roll the pastry out and line an 11 x 33cm rectangular, fluted tart tin. (The pastry may break up as you work it, so patch over any broken bits.) Keep any excess trimmings. Chill the tart case in the fridge or freezer for 20 mins. While the tart case is chilling, tip all the ingredients for the parfait into a clean food processor with a generous pinch of salt and a good grinding of pepper. Blitz until the mix is as smooth as it’s going to get, then push through a sieve into a jug and set aside. Heat oven to 200C/fan 180C/gas 6. Line the tart case with greaseproof paper and baking beans, then bake on a baking tray for 15 mins. Remove from the oven and remove the paper and beans. Check for any small holes or cracks in the pastry and patch up with the reserved trimmings. Place back in the oven for 15 mins, until golden. Remove from the oven and lower the oven to 120C/fan 100C/ gas ½. When the oven has cooled suitably, slide the tart case back into it, then fill as far as you can with the parfait mix. Bake the tart for 20 mins until just set. Leave to cool, trim any untidy edges, then remove from tin. To serve, cut the tart into 6 slices. Place on plates, then place small blobs of caramelised onions and a scattering of hazelnuts around the tart. Neatly place a few salad leaves around and drizzle everything with oil and vinegar. Arrange 2 fig quarters on top of each slice and serve.",
        "name": "Silky Chicken Liver Parfait Tart",
        "ingredients": [
          "250g plain flour",
          "2 tsp thyme leaves",
          "140g cold butter, cut into cubes",
          "1 egg yolk",
          "1 tbsp milk",
          "140g chicken livers",
          "142ml pot double cream",
          "1 egg yolk",
          "1 tbsp brandy",
          "2 tsp port",
          "1 small garlic clove",
          "1 shallot, roughly chopped",
          "couple of thyme branches",
          "pinch of grated nutmeg",
          "6 tbsp caramelised onion from a jar",
          "50g toasted hazelnuts, cracked",
          "3 handfuls small salad leaves",
          "6 tbsp walnut oil or olive oil",
          "2 tsp balsamic vinegar",
          "3 figs, quartered"
        ]
      },
      {
        "instructions": "Put the chicken thighs into a pan with the stock and a string-tied bundle of 2 bay leaves, a few of the thyme sprigs and a little of the parsley. Add a few leek trimmings, the peppercorns and ½ tsp salt. Add water to just cover the meat, if needed. Bring to the boil, then cover and gently simmer for 30 mins. Meanwhile, lightly butter a 900g loaf tin (ours was 12cm x 22cm x 7cm) and line with cling film, leaving plenty of overhang. Melt the butter in a  , then add the leeks, shallots and some seasoning. Cook for 10 mins over a medium heat until starting to colour. Add the bacon and garlic and cook for 2 mins more until the bacon is cooked through. Leave to cool. Add the chicken breast to the stock mixture and top up with hot water to cover. Bring to the boil, then cover and simmer gently for another 20 mins. When ready, the chicken breast will be cooked through and the thigh meat will pull away easily from the bones. Lift the meat from the pan, drain the stock and leave to cool until it is just warm. Discard the bones and any knobbly bits, then roughly chop the chicken. Stir into the leek mixture, along with 2 tsp more thyme leaves, the apricots and the brandy. Soak the gelatine in cold water for 5 mins until floppy. Squeeze out the excess water, stir into 300ml of the warm stock, then mix with the chicken. Put a few bay leaves in the base of the tin, then spoon the chicken mixture on top and press down well. Cover with the cling film. Leave to cool, then chill thoroughly – overnight is best.  To serve, slice the terrine while it's still wrapped in cling film, then carefully peel the cling film off each slice. Drizzle the toast slices with olive oil and grill until golden brown and crisp, then sprinkle with a little salt. Serve the terrine with the toast and our yogurt piccalilli & crisp kale salad.",
        "name": "Chicken Terrine With Leeks & Apricots",
        "ingredients": [
          "1kg chicken thighson the bone, skin removed",
          "500ml fresh chicken stock(you can buy this ready-made)",
          "2 bay leaves, plus more to decorate",
          "handful thyme sprigs",
          "handful parsley",
          "2 leeks, finely chopped (keep the trimmings)",
          "6 black peppercorns",
          "30g butter, plus more for the tin",
          "1 large or 2 smaller banana shallots, finely chopped",
          "50g smoked streaky baconor pancetta, finely chopped",
          "1 large garlic clove, finely chopped",
          "2 chicken breasts, on the bone if possible, skin removed",
          "50g soft dried apricots, chopped",
          "3 tbsp brandy",
          "4 sheets leaf gelatine",
          "toastdrizzled with olive oil, to serve (we used Crosta & Mollica Pane Pugliese)"
        ]
      },
      {
        "instructions": "Heat 1 tbsp of the butter in a non-stick frying pan over a medium heat. When the butter is foaming, add the chicken livers and fry for 2 mins each side. Stir the crushed garlic, some of the thyme and Madeira into the pan with the livers. Fry for 2 mins, letting the Madeira simmer. Transfer the mixture to a food processor, reserve 200g of the butter and add the rest to the processor. Blend everything to a smooth paste. Season to taste, then spoon into 4 x 70ml clip-top jars. Melt the reserved butter in a medium frying pan and add the sliced garlic. Turn the garlic in the butter until slightly golden. Pour into the 4 jars of pâté, ensuring a few slices of garlic and the remaining thyme leaves go in each jar, and chill in the fridge for at least 4 hrs, or until set. Can be made up to 2 days in advance. Before serving, toast the brioche, then cut into triangular quarters for serving. Stir the diced apple through the chutney. Serve the pâté on small wooden boards with the toasted brioche, cornichons and chutney.",
        "name": "Chicken Liver PâTé",
        "ingredients": [
          "375g unsalted butter",
          "400g chicken livers, trimmed",
          "2 large garlic cloves, 1 crushed, 1 finely sliced",
          "3 thyme sprigs, leaves only",
          "3 tbsp madeira",
          "4 slices brioche",
          "1 Bramley apple, cored and diced",
          "onion chutney, to serve",
          "cornichons, to serve"
        ]
      }
    ]
  },
  "code": 200
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact).

---

## Updates
Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms) and all legal documents and agreements.

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2024 APIVerve, and Evlar LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.