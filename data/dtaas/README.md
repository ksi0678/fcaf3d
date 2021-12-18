### Prepare DTAAS

1. Put DTAAS dataset to `DTAAS` directory.

2. Create labels using the command below
```bash
python data/dtaas/python/create_labels.py
```

3. Create depth data using the command below
```bash
python data/dtaas/python/create_points.py
```

4. Create DTAAS data pickle using the command below
```bash
python tools/create_data.py dtaas --root-path ./data/dtaas --out-dir ./data/dtaas --extra-tag dtaas
```

### Train a model with the DTAAS dataset.
```bash
bash tools/dist_train.sh configs/fcaf3d/fcaf3d_dtaas-3d-9class.py 2
```
