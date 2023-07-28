# Configuration introduction
We conducted the experiment utilizing AWS Celebrity Face Rekognition (ACFR). Due to ACFR's incompatibility with the Google Colab platform, we made the API calls within the vscode + Jupyter plugin environment. We employed Google Colab to take advantage of its High GPU capabilities for stable diffusion and fine-tuning tasks. To utilize the AWS Celebrity Rekognition API, you will need to provide your own API key and API secret in the code. The current placeholders in the code are not valid. Please ensure that you have obtained the necessary API credentials from AWS.

# Project structure
[**heads**](https://github.com/EricW1118/ComVisionProject/main/heads) : All the head photos from Kagle \
[**headsets**](https://github.com/EricW1118/ComVisionProject/main/headsets): Head photos randomly selected from <heads> folder \
[**dev.csv**](https://github.com/EricW1118/ComVisionProject/main/dev.csv): Original dataset with URL, Name, and Face Region listed in each row \
[**dev**](https://github.com/EricW1118/ComVisionProject/main/dev): Images downloaded using code <**download_preprocess.ipynb**> from original dataset file <**dev.csv**> \
[**Encryption_Results.py**](https://github.com/EricW1118/ComVisionProject/main/Encryption_Results.py): Code for encryption method, this code should be run under AWS notbook \
[**Encrypt_config.csv**](https://github.com/EricW1118/ComVisionProject/main/Encrypt_config.csv): Recognition rate of 300 faces using code <**Encryption_Results.py**> \
[**StableDiff.ipynb**](https://github.com/EricW1118/ComVisionProject/main/StableDiff.ipynb): Code for generating images using stable diffusion Image2Image pipeline without fine-tuning \
[**Fine_tuning.ipynb**](https://github.com/EricW1118/ComVisionProject/main/Fine_tuning.ipynb): Fine-tuning Stable Diffusion with Text2Image pipeline \
[**concepts_list.json**](https://github.com/EricW1118/ComVisionProject/main/concepts_list.json): The instant prompts and class prompts generated by code <**Fine_tuning.ipynb**> for fine-tuning \
[**inpaint.ipynb**](https://github.com/EricW1118/ComVisionProject/main/inpaint.ipynb): Code for Inpaint pipeline in for stable diffusion <**not completed**, considered as future work > \
[**commonfuns.py**](https://github.com/EricW1118/ComVisionProject/main/commonfuns.py): Code for often used functions during the project \
[**download_preprocess.ipynb**](https://github.com/EricW1118/ComVisionProject/main/download_preprocess.ipynb): Code for downloading and preprocessing the images from <**dev.csv**>  \
[**cv_main.ipynb**](https://github.com/EricW1118/ComVisionProject/main/cv_main.ipynb): Code for the regular methods <Gaussian noise, eye patches, line through eyes, leopard spots> \
[**config.csv**](https://github.com/EricW1118/ComVisionProject/main/config.csv): Recognition rate after experiments in <**cv_main.ipynb**>, use this result to plot the diagram, curve and make comparison tables. \
[**requirements.text**](https://github.com/EricW1118/ComVisionProject/main/requirements.text) Configuration file for fine-tuning code \
[**train_dreambooth.py**](https://github.com/EricW1118/ComVisionProject/main/train_dreambooth.py): training tool from **dream booth**, slightly modified because of some compile error, not use it directly.
