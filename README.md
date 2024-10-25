# Chicken Disease (coccidiosis) Classification

### Workflow Sequence:

1. config.yaml
2. secrets.yaml*
3. params.yaml
4. entity
5. configuration manager -> src config
6. components
7. pipeline
8. main.py
9. dvc.yaml

### Tensorboard cmd:

```
tensorboard --logdir artifacts/prepare_calbacks/tensorboard_log_dir/
```

### DVC:

1. ```
   dvc init
   ```
2. ```
   dvc repro
   ```
3. ```
   dvc dag
   ```

### Flask App:

Run app on local host:

```
py app.py
```

local host:

```
http://127.0.0.1:8080/
```

Train model through local host:

```
http://127.0.0.1:8080/train/
```
