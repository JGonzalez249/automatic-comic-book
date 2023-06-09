<h1>Visual Generation Project</h1>

<h2>Artist Statement</h2>
<p>When looking to create something using visual generative AI, there were many options to choose from, however, when researching different types of AI art, I can across a recently published manga called Cyberpunk: Peach John. Using that work as inspiration, I wanted to make a stable diffusion that generated manga or comic book pages through the use of prompts. While the main goal is to have randomly generated comic book pages, I wanted to make a consistent character so that people can recognize that the “story” is about them. However, this is much more difficult than just telling stable diffusion to generate one character, while you can provide that prompt to generate a character, it still came out as a random character just wearing similar clothes. The point isn't to make a entire comic but to generate comic images with generative AI as an assistant tool to help design manga or comics while having the main subject matter part of the page.</p> 

<p>So looking at the work done by Rootport, the creator of Cyberpunk: Peach John, they mentioned using distinctive characteristics in order for the reader to recognize characters. Since my intent was to make a comic generator with a consistent character, I tried to replicate how they did it. Using a style that I found works well in comic book format via a stable diffusion google colab, I heavily used negative prompts in order to reliably generate a consistent character. Since I can’t have just a single character appear in a comic book, I also needed to adjust prompt to generate random characters into the panels. Using trial and error, I manage to make a consistent character, however, sometimes the art style won’t stay to the designated one I put into the prompt unless I specifically state that I want to use this style for any subject or random people don't generate all, I specifically used a Cyberpunk diffusion that uses Cyberpunk Edgerunners as base for its training.</p>

<p>In terms of methods, I tried various methods to get stable diffusion to work, including using inpainting, merging models, and even using other methods like Midjourney and Dreamstudio to test prompts and see what other styles work. However, in the end, I chose to research a little more into prompt engineering in order to have the AI look a specific parts of both positive and negative prompts. While it helps to have the AI focus of what I want from the prompts, the CFG scale and steps vastly change what is generated. However, even with these random generations, my character stays somewhat consistent and recognizable. This shouldn't be something that should be used in a final production product but might be a good staring point to starting your own rough draft to get a consistent character and maybe even panel design.</p>

<h2>Google Colab</h2>

<h3>(Use Nightly, use Stable if Nightly doesn't work)</h3>

[![Open In Colab](https://user-images.githubusercontent.com/54370274/224839806-8720fb19-9c7d-46a2-8d7c-de3afb39c11f.svg)](https://colab.research.google.com/github/camenduru/stable-diffusion-webui-colab/blob/main/lite/cyberpunk_anime_diffusion_webui_colab.ipynb) | [![Open In Colab](https://user-images.githubusercontent.com/54370274/224839804-50c0c18b-3960-4a1c-b7fa-3c7074b11779.svg)](https://colab.research.google.com/github/camenduru/stable-diffusion-webui-colab/blob/main/stable/cyberpunk_anime_diffusion_webui_colab.ipynb) | [![Open In Colab](https://user-images.githubusercontent.com/54370274/224839802-95968900-392b-4b30-ad75-aeac13675e1b.svg)](https://colab.research.google.com/github/camenduru/stable-diffusion-webui-colab/blob/main/nightly/cyberpunk_anime_diffusion_webui_colab.ipynb) | cyberpunk_anime_diffusion_webui_colab <br /> (Use the tokens `dgs illustration style` in your prompts for the effect.) <br /> [DGSpitzer/Cyberpunk-Anime-Diffusion](https://huggingface.co/DGSpitzer/Cyberpunk-Anime-Diffusion)

<h3>Use these prompts and settings to get the effect in stable diffussion</h3>
You can change the character discription to fit your subject matter.

        (an anime girl in dgs illustration style, long black hair and red highlights, hair bangs, blue eyes, peach colored face, (wearing open black coat), body suit:1.3), zoomed out, (cyberpunk city:1.2), raining, neon, (manga-style, text bubbles, comic panels:1.6), low key, darker color scheme, <lora:epiNoiseoffset_v2:0.7>, 8k, ultra detailed, clarity, intense
        Negative prompt: bad-artist, bad-image-v2-39000, (bad_prompt_version2:0.8), EasyNegative,  NG_DeepNegative_V1_75T, short hair, pony tail, single image, no panels, extra limbs, comic book, different color eyes
        Steps: 20, Sampler: DPM++ SDE Karras, CFG scale: 7, Seed: 866203473, Face restoration: CodeFormer, Size: 704x704, Model hash: ab55b3722e, Model: Cyberpunk-Anime-Diffusion

<h2>Example</h2>

[![Automatic Comic Generation, Stable Diffusion](https://res.cloudinary.com/marcomontalbano/image/upload/v1680134246/video_to_markdown/images/youtube--yfPbuoxZWjY-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/JDzGo_jpYfk "Stable Diffusion - Automatic Comic Generator")


