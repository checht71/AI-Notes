This is a method of port forwarding you can use so that you can use Jupyter Notebook on your remote server from your local computer.

If you are using Lambda Labs, you will have to update jupyter notebook

If you do not see the token, ssh in with a new terminal and type `jupyter notebook list`.
Keep this window open, you will need to copy the token in order to open the notebook properly.

[Video: Run Jupyter notebook from a remote server](https://www.youtube.com/watch?v=ZhVdA2jSCuA)

Next you need to SSH in with the following command to begin tunneling:
```bash
ssh ubuntu@124.1234.1235 -N -f -L localhost:7777:localhost:7000
```

Then on your computer open a browser and go type localhost:7777 into the URL bar and the notebook should pop up. You need to get your 