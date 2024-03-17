# README

This repository contains a Jupyter notebook that can be used to download a large number of images from the website [thispersondoesnotexist.com](https://thispersondoesnotexist.com/). 

- The images are generated by a GAN (Generative Adversarial Network) and are not real people. 
- DeepFace is used to identify if the generated image is male or female and then the image is saved in the respective folder, with the person's name as the filename.
- The images are generated in on the fly from an `input.csv` file you provide that contains a list of people's Names & Genders.
- You can also supply an age range for the people you want to generate images for.
- The images are cropped to remove the stupid watermark crap that the website adds to the bottom of the images.

## How to use

1. Clone the repository to your local machine.
2. Open the Jupyter notebook `bulk-download-images.ipynb` in Jupyter.
3. Create an `input.csv` file with the following columns: `Name` and `Gender`.
4. Run the Jupyter notebook!

Important: Make sure that your csv follows the format in the `input-template.csv` example (no space before the gender)

## Helpful Prompts

To get a list of names to use, I recommend using the free ChatGPT 3.5 and a prompt like this:

```markdown

create a bullet point list of 200 `firstname lastname` pairs that are common american names for MALES in this format:

- Firstname Lastname,Gender

<|###|>
IMPORTANT:

* make sure to do the number i say. do not cut it short
* make sure to give a large variety of different firstnames 
* make sure to give a large variety of different lastnames
<|###|>
```