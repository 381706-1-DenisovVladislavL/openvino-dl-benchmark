# ������������ �������� �������

## ������������ �������� ������� � ���������� ������

```bash
inference_sync_mode.py [TBD]
```

��������� �������:
- [TBD]

## ������������ �������� ������� � ����������� ������


### ������ �������������
```bash
python inference_async_mode.py \
    -t classification -i <path_to_image>/image.png \
    -m <path_to_model>/<model_name>.xml -w <path_to_weights>/<model_name>.bin \
    -r 1 --labels <path_to_labels>/image_net_synset.txt -ni 10
```

��������� ����������: ���������� ����� (��� ������������ ������),
� �������� ��������� ������ �� �����������.


### ������ ��������������
```bash
python inference_async_mode.py \
    -t detection -i <path_to_image>/image.png \
    -m <path_to_model>/<model_name>.xml -w <path_to_weights>/<model_name>.bin \
    -r 1 -d GPU -ni 10
```

��������� ����������: ���������� ������� ������� �� �����������,
� ����� ������� ��� ��������� � ������� ��������� �������� ���������
�����������, ������� ��� � �������������.


### ������ ������������� �����������
```bash
python inference_async_mode.py \
    -t segmentation -i <path_to_image>/image.png \
    -m <path_to_model>/<model_name>.xml -w <path_to_weights>/<model_name>.bin \
    -r 1 --color_map <path_to_color_map>/color_map.txt -ni 10
```

��������� ����������: ��������� ��������� ������� �� ������ �� �� ���������,
������ �� ���� �� ���� ��������, �� ���� ��� �� �� �������������.


��������� �������:
-    `-t / --model_type`     - ������, ������� ���������� ������.
-    `-i / --input`          - ���� �� �������� ��� ����� � ����������. 
                               ���������� �������� ".jpg", ".png", ".bmp" � �.�.
-    `-m / --model`          - ���� �� ������.
-    `-w / --weights`        - ���� �� ����� ������.
-    `-r / --request`        - ������������� �������������  ����� 
                               �������� �� ������������� ���������. 
                               ��������� ��������: 1 � 2.
-    `--labels`              - ���� �� ����� �������.
-    `-d / --device`         - ����������, �� ������� ����� ����������� ������.
-    `--color_map`           - ���� �� ����� ������.
-    `-ni / --number_iter`   - ����� ��������.