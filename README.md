# MultiSum: A Dataset for Multimodal Summarization and Thumbnail Generation of Videos

## Usage

### Set up Environment

Create a conda virtual environment and activate it.

```
conda env create -f MultiSum/multisum.yml
conda activate multisum
```

### Download Datasets and Preprocessing

Please download the video, keyframe, thumbnail features from this [link](https://drive.google.com/drive/folders/1QRtU32oiTbAzU9swn1ZFFg0hxmpz3a3k?usp=sharing).

We provide the scripts [keyframe_feature.py, text_feature.py, video_feature.py] to create the features for the whole text environment.
We provide code to generate the segmented text environment data in seg_video_feature.py and video_feature_multisum.py.

After preprocessing, there should be 2 sets of training, validation, test sets.
{set_name}.tsv is for the whole sentence and video environment and {set_name}_2.tsv is for the segmented video environment.

Please place them in MultiSum/src/data.

### Training and Evaluation

For training, please cd into MultiSum/src/runtime and run the following command:

```
sh train.sh
```

For evaluation, stay in the same folder and run the following command:

```
sh eval.sh
```

For thumbnail generation, stay in the same folder and run the following command:

```
python generate_thumbnail.py
```

### Citation

```
@inproceedings{Qiu2023MultiSumAD,
    title={MultiSum: A Dataset for Multimodal Summarization and Thumbnail Generation of Videos},
    author={Jielin Qiu and Jiacheng Zhu and William Han and Aditesh Kumar and Karthik Mittal
            and Claire Jin and Zhengyuan Yang and Linjie Li and Jianfeng Wang
            and Bo Li and Ding Zhao and Lijuan Wang},
    journal={arXiv preprint arXiv:2306.04216},
    year={2023}
```

### Acknowledgements

We appreciate the public codebase from [MLASK](https://github.com/ufal/MLASK).

## License

This project is licensed under the CC BY-NC-SA License.

