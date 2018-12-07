# ������������ �������� �������

## ������������ �������� ������� � ���������� ������

```bash
inference_sync_mode.py [TBD]
```

��������� �������:
- [TBD]

## ������������ �������� ������� � ����������� ������

```bash
python inference_async_mode.py \
    -t classification -i <path_to_image>/image.png \
    -m <path_to_model>/model.xml -w <path_to_weights>/model.bin \
    -r 1 --labels <path_to_labels>/image_net_synset.txt

python inference_async_mode.py \
    -t detection -i <path_to_image>/image.png \
    -m <path_to_model>/model.xml -w <path_to_weights>/model.bin \
    -r 1 -d GPU

python inference_async_mode.py \
    -t segmentation -i <path_to_image>/image.png \
    -m <path_to_model>/model.xml -w <path_to_weights>/model.bin \
    -r 1 --color_map <path_to_color_map>/color_map.txt
```

��������� �������:
-    `-t / --model_type`   - ������, ������� ���������� ������.
-    `-i / --input`   - ���� �� �������� ��� ����� � ����������. 
                       ���������� �������� ".jpg", ".png", ".bmp" � �.�.
-    `-m / --model`   - ���� �� ������.
-    `-w / --weights`   - ���� �� ����� ������.
-    `-r / --Request`   - ������������� ������������� �������� infer requests,
                          ������� ������ ���� �������. ��������� ��������: 1 � 2.
-    `--labels`   - ���� �� ����� �������.
-    `-d / --device`   - ����������, �� ������� ����� ����������� ������.
-    `--color_map`   - ���� �� ����� ������.