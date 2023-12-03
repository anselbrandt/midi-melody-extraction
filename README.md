# Midi Melody Extraction

This is a fork of [midi_melody_extraction
](https://github.com/bytedance/midi_melody_extraction)

[A deep learning method for melody extraction from a polyphonic symbolic music representation](https://archives.ismir.net/ismir2022/paper/000091.pdf)

[data corpus](https://github.com/music-x-lab/POP909-Dataset/tree/master/POP909)


Original bash script:

```
python3 LStoM/process_data.py -i __path_to__POP909-Dataset/POP909 -o ./processed_data -q $@
python3 LStoM/create_stats_dict.py -i ./processed_data -o ./yaml_files $@
python3 LStoM/train.py -sd ./yaml_files/stats_config_train_valid.yaml -ds ./yaml_files/data_split.yaml -o ./model_results -of ./model_results/test_model.pt -v $@
```