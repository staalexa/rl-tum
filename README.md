# RL-Checkers

Entrypoint of the game is `menu.py`

Requirements: `pip install -r requirements.txt`

Training can be done with `python train_model.py`. As code was optimized, auto updating the model is not possible. To replace the current model, delete all files from the checkpoints folder. Then train the model and rename the file to `best_model.pth`. Then you can play against it. 

> Remark


Training is optimized for H100 GPUs and does not perform well on CPU driven systems or on consumer grade GPUs.

---
The `infra` folder contains terraform scripts for the AWS environment. In the `older_version_with_aws_support` you can find older code, which fully works with s3 buckets to store models like in the presentation. I chose to reevaluate the training to try to fix model convergence, but the old version as presented is also in that folder. Entrypoint for the code is `menu.py` but with lots of unused files still existing.