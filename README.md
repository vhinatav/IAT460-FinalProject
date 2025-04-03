# Emotion-Based Colour Palette Generator

## Overview
This system is a rule-based system that generates a colour palette based on emotions. Each emotion is associated with a predefined set of colours, and when the user inputs three emotion words, the program randomly selects colours from the corresponding palettes and displays them as an image.

#### Use Cases
1. **For Designers and Creators:** This tool can assist in selecting colours that align with the emotions you want to convey in your designs. For example, if you are working on branding for a company and want to express trust, you can use this tool to find colour combinations that are associated with trust.
2. **For Fun and Inspiration:** Anyone can use the system for creative inspiration. Whether you're an artist, a hobbyist, or simply curious about emotional colour combinations, this tool generates random yet meaningful palettes that could spark new ideas for your next project.

## How It Works
1. The user provides three emotions as input (e.g., love, joy, sadness).
2. The program checks a predefined dictionary of emotion-to-colour mappings.
3. Two random colours are selected from each emotion's palette.
4. If an emotion is not found in the dictionary, it is ignored, and a warning is displayed.
5. The selected colours are used to generate a visual representation.
6. The final colour palette is displayed as an image.

#### Rule-Based System
This system was developed using a rule-based AI system. Here is how it works:
- Rule-Based AI relies on predefined rules and mappings instead of learning from data. In this case, the mapping of emotions to colours is manually defined in a dictionary.
- The system is deterministic, meaning it will always produce the same output for the same input (in this case it is a bit randomized), unlike machine learning systems that learn from patterns in data.
- In the context of this project, the rule-based approach was chosen as it allows for a clear and simple representation of emotions with colours, and it aligns with the course materials.

The system checks if the entered emotion is present in the predefined dictionary. If so, it selects colours from the corresponding palette. If the emotion is not found, a warning is displayed, and no colour is selected for that emotion.

## Notes

#### Customization
- The colour_palettes dictionary can be edited to add or modify colours for emotions.
- Change the number of selected colours per emotion by modifying random.sample(colour_palettes[keyword], 2).
- Adjust image size by modifying img_height and img_width in generate_palette_image().

#### Limitations
- The system is rule-based, meaning it does not learn or infer relationships between emotions and colours dynamically.
- If an emotion is not found in the dictionary, it is skipped instead of inferred.

#### Possible Future Implementation
- Given that the current set of emotion words and colour combinations is limited, expanding the range of combinations could allow for a broader scope of user input. One potential approach would be to modify the system to read from a larger dataset sourced from a data file.
- Additionally, instead of solely using colours, it would be both interesting and useful to represent emotions with generative illustrations or images, further enhancing the user experience.
