# *🎥 VIDEO-TRANSLATE 🎴*
Get ready to elevate your audio/video game! 🎙️ Transform your videos into captivating masterpieces as you sync voices flawlessly. 🎬 Whether you're a pro or just starting out, our project's user-friendly interface makes dubbing a breeze. 💻 Fine-tune pitch, tone, and timing with precision to breathe life into characters like never before. 🌟 Break down language barriers and reach global audiences with ease. 🌍 Say hello to seamless multilingual content creation! 🌐 Experience the thrill of storytelling on GitHub today. 🚀 Revolutionize your production process and unleash your creativity! 🎉 Let SoniTranslate be your ultimate tool for immersive audio transformation. 🔥


## 🎥 How To Use 🎴
1. Sign-in to your Google Account: https://www.google.com/gmail/about/

2. Click this link to open the project in Google Colab: https://colab.research.google.com/github/R3gm/SoniTranslate/blob/main/SoniTranslate_Colab.ipynb

## 🎥 Now In Google Colab 🎴
1. Run the code for installing the requirements for NERV Translate.

2. Sign-in or create a https://huggingface.co/ account. Also don't forget to verify your Hugging Face account through confirmation link send to your Gmail account. 

3. Once the code is finished running:

   Click: https://huggingface.co/pyannote/speaker-diarization , Fill out the details and click on "Agree and access repository."

   Similarly,

   Click: https://huggingface.co/pyannote/segmentation , Fill out the details and click on "Agree and access repository."

5. At last, click on https://huggingface.co/settings/tokens and select the "New Token" option. Generate the token and copy it.

6. Now come back to Google Colab and paste your copied token the the given box below and "Run The Web App."

7. Run the PUBLIC URL.

    Example URL: https://2ed1eddebd5548fd77.gradio.live


## *🔥 Finally, play with the settings and enjoy Dubbing! 🔥*


## 🎥 UI 🎴
![UIST](https://github.com/Hrishikesh-Gavai/NERV-TRANSLATE/assets/168000487/52e0e364-2bdd-42b2-9c0f-362994bda564)


## 🎥 Example Of Dubbing 🎴
Original



https://github.com/Hrishikesh-Gavai/NERV-TRANSLATE/assets/168000487/a3ef58bb-5749-4230-836c-c5e883f15f97

Hindi Dubbed



https://github.com/Hrishikesh-Gavai/NERV-TRANSLATE/assets/168000487/c97bfa76-ab9a-457a-bccb-63d8b5f484d7


# 🎥Install Locally (Installation tested in Linux) 🎴
### Before You Start

Before you start installing and using SoniTranslate, there are a few things you need to do:

1. Install the NVIDIA drivers for CUDA 11.8.0, NVIDIA CUDA is a parallel computing platform and programming model that enables developers to use the power of NVIDIA graphics processing units (GPUs) to speed up compute-intensive tasks. You can find the drivers [here](https://developer.nvidia.com/cuda-toolkit-archive). Follow the instructions on the website to download and install the drivers.
2. Accept the license agreement for using Pyannote. You need to have an account on Hugging Face and `accept the license to use the models`: https://huggingface.co/pyannote/speaker-diarization and https://huggingface.co/pyannote/segmentation
3. Create a [huggingface token](https://huggingface.co/settings/tokens). Hugging Face is a natural language processing platform that provides access to state-of-the-art models and tools. You will need to create a token in order to use some of the automatic model download features in SoniTranslate. Follow the instructions on the Hugging Face website to create a token.
4. Install [Anaconda](https://www.anaconda.com/). Anaconda is a free and open-source distribution of Python and R. It includes a package manager called conda that makes it easy to install and manage Python environments and packages. Follow the instructions on the Anaconda website to download and install Anaconda on your system.
5. Install Git for your system. Git is a version control system that helps you track changes to your code and collaborate with other developers. You can install Git with Anaconda by running `conda install -c anaconda git -y` in your terminal (Do this after step 1 in the following section.). If you have trouble installing Git via Anaconda, you can use the following link instead:
   - [Git for Linux](https://git-scm.com/download/linux)

Once you have completed these steps, you will be ready to install SoniTranslate.

### Getting Started

To install SoniTranslate, follow these steps:

1. Create a suitable anaconda environment for SoniTranslate and activate it:

```
conda create -n sonitr python=3.10 -y
conda activate sonitr
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
```

2. Clone this github repository and navigate to it:
```
git clone https://github.com/r3gm/SoniTranslate.git
cd SoniTranslate
```

3. Install required packages:

```
pip install -r requirements_base.txt -v
pip install -r requirements_extra.txt -v
pip install onnxruntime-gpu
```

4. Install [ffmpeg](https://ffmpeg.org/download.html). FFmpeg is a free software project that produces libraries and programs for handling multimedia data. You will need it to process audio and video files. You can install ffmpeg with Anaconda by running `conda install -y ffmpeg` in your terminal. If you have trouble installing ffmpeg via Anaconda, you can use the following link instead: (https://ffmpeg.org/ffmpeg.html). Once it is installed, make sure it is in your PATH by running `ffmpeg -h` in your terminal. If you don't get an error message, you're good to go.

5. Optional install:

After installing FFmpeg, you can install these optional packages.


[Piper TTS](https://github.com/rhasspy/piper) is a fast, local neural text to speech system that sounds great and is optimized for the Raspberry Pi 4. Piper is used in a variety of projects. Voices are trained with VITS and exported to the onnxruntime.

```
pip install -q piper-tts==1.2.0
```

[Coqui XTTS](https://github.com/coqui-ai/TTS) is a text-to-speech (TTS) model that lets you generate realistic voices in different languages. It can clone voices with just a short audio clip, even speak in a different language! It's like having a personal voice mimic for any text you need spoken.

```
pip install -q -r requirements_xtts.txt
pip install -q TTS==0.21.1  --no-deps
```


### Running SoniTranslate

To run SoniTranslate locally, make sure the `sonitr` conda environment is active:

```
conda activate sonitr
```

Setting your Hugging Face token as an environment variable in Linux:

```
export YOUR_HF_TOKEN="YOUR_HUGGING_FACE_TOKEN"
```

Then navigate to the `SoniTranslate` folder and run either the `app_rvc.py`

```
python app_rvc.py
```
When the `local URL` `http://127.0.0.1:7860` is displayed in the terminal, simply open this URL in your web browser to access the SoniTranslate interface.

### Stop and close SoniTranslate.

In most environments, you can stop the execution by pressing Ctrl+C in the terminal where you launched the script `app_rvc.py`. This will interrupt the program and stop the Gradio app.
To deactivate the Conda environment, you can use the following command:

```
conda deactivate
```

This will deactivate the currently active Conda environment sonitr, and you'll return to the base environment or the global Python environment.

### Starting Over

If you need to start over from scratch, you can delete the `SoniTranslate` folder and remove the `sonitr` conda environment with the following set of commands:

```
conda deactivate
conda env remove -n sonitr
```

With the `sonitr` environment removed, you can start over with a fresh installation.

## Command line arguments

The app_rvc.py script supports command-line arguments to customize its behavior. Here's a brief guide on how to use them:

| Argument command | Default | Value | Description |
|------------------|---------|-------|-------------|
| --theme          | Taithrah/Minimal | String | Sets the theme for the interface. Themes can be found in the [Theme Gallery](https://huggingface.co/spaces/gradio/theme-gallery). |
| --language       | english | String | Selects the interface language. Available options: arabic, azerbaijani, chinese_zh_cn, english, french, german, hindi, indonesian, italian, japanese, korean, marathi, polish, portuguese, russian, spanish, swedish, turkish, ukrainian, vietnamese. |
| --verbosity_level| info    | String | Sets the verbosity level of the logger: debug, info, warning, error, or critical. |
| --public_url     |    | Boolean | Enables a public link. |
| --logs_in_gui    |    | Boolean | Shows the operations performed in Logs (obsolete). |

Example usage:
```
python app_rvc.py --theme aliabid94/new-theme --language french
```
This command sets the theme to a custom theme and selects French as the interface language.
Feel free to customize these arguments according to your preferences and requirements.

## 🎥 Credits 🎴
1. Team NERV: KKWIEER- F.Y.BTech Computer Engineering.
2. R3gm (https://github.com/R3gm): SoniTranslate (https://github.com/R3gm/SoniTranslate?tab=readme-ov-file)
