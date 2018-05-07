# ACTIVATION FUNTION


> Activatio function is a function which takes a input or set of inputs and gives a performs operation on that and gives single output. It is middle betwwn the input and the neuron which fires according to the input stimuli.


![IMAGE ALT ACTIVATION FUNCTION](https://www.geeksforgeeks.org/wp-content/uploads/33-1-1.png)

EQUATION

 
 $$output = {\sum({Weight*Input}+Bias)}.$$
 
> The value of the input can anything from the value of -infinity to +infinity, the neuron doesn't know the value for the firing pattern. We appy a activation function on the input or set of inputs which gives a output in a certain range which tells the neron to fire or not to fire.
 

There are many activation function in the neural network.
Ex:
1. Step function
2. Linear function
3. Sigmoid Function
4. ReLU (Rectified Linear Unit)
5. Leaky ReLU


## 1.Step Function

  $$output =  \begin{cases}
  \displaystyle 0 \ \ \ \ \ \ \ for\     \ x < 0 \\\\
	
  \displaystyle 1   \ \ \ \ \ \ \ for\     \ x \ge 1
  \end{cases}$$
	

![IMAGE ALT STEP FUNCTION](http://www.saedsayad.com/images/ANN_Unit_step.png)


It is a very basic activation function, which activates a neurin on the basis of a threshold value.If the input value is greater than the threshold value the neron will be activated. If the neuron is less than the threshold value the neron will not triggered.


Works fine with the binary classifier kind of value. Activate if value 1 or deactivate for 0. What if the you need to trigger for 30%. Which will not be possible in the step avtiv ation function


## 2. Linear function

$$output = {{c*x}}.$$

![IMAGE ALT LINEAR FUNCTION](https://www.researchgate.net/profile/Valerio_Lo_Brano/publication/259843708/figure/fig9/AS:322849555402767@1453984740551/The-most-common-activation-functions-a-step-function-b-linear-function-c-sigmoid.png)

It is a linear function, where output is directly proportional to the input. In this function if the more than neuron fires, then we take the max and drecide based on that.


Even this is not binary activation function, no matter what a linear function results a another linear equation. TRaking this no matter how many layer we use this linear function, this will end up giving other linera values. Hence single activatio function is always equal to nth activation function.


## 3. Sigmoid Function

$$output = {{ 1 \over 1 +e^{-x} }} = {{e^{x}\over e^{x}+1}}$$

![IMAGE ALT SIGMOID FUNCTION](https://qph.fs.quoracdn.net/main-qimg-05edc1873d0103e36064862a45566dba)

Sigmoid function is one of the widely used activation function in neural network. It is a non linear equation, This function makes a signaficant change in the output depending on the input provided and also it has a tendency to make to set value to either end of the Y axis, which helps in clear distinction on output.


And also output of the sigmoid function is always be in the range of (0, 1) compared to (-inf, +inf) value. We have clear range of values, Which helps in the neuron triggering.


It also suffers fro the `"vanishing gradients"` problem, ie there are large region of input space which results results very small change in the output.In other words this problem creates a hard problem for the network to learn because of the small change in the output even large change in the iput. This problem worsen as the number of layers increases in the architecture.


## 4. ReLU (Rectified linear unit)

$$output \ \ A(X) = {{ max(0, x) }}$$


$$output \ f(x) =  \begin{cases}
  \displaystyle 0 \ \ \ \ \ \ \ for\     \ x < 0 \\\\
	
  \displaystyle x   \ \ \ \ \ \ \ for\     \ x \ge 0
  \end{cases}$$


![IMAGE ALT ReLU FUNCTION](https://leonardoaraujosantos.gitbooks.io/artificial-inteligence/content/image_folder_4/Relu.jpeg)


ReLU is a nonlinear equation in positive axis. It is a simple equation which outputs x if x is positive, 0 for all other (-ve)values. The range of ReLU varies from (0, +inf), which is good for activation.

The important advantage of the ReLU is less costly comapring to all the other activation programs. Considering Sigmoid almost all the neuron gets trigered in a analog manner, which means all activations will be processed t get the resultant output, which means it is dense. For processing all the activations take lot of computation and time, it is costly. The ideal scenario is few neuron not to activate, making activation sparse, efficient and less costly.


Considering ReLU behavior with random initialized weights and almost 50% of the output results 0 because of the characteristics of the ReLU, which means less neuron firing, lighter network, less costly.


ReLU also has few demerits, because of horizontal line in ReLU(-ve X axis) the gradients slides towards 0. The activation of the neurons in the region of ReLU, gradient will be zero because of the weights will not be adjusted during the descent. Which means the those neurons which are going in this state will stop responding to variations in the error or input (because the gradient value is 0). This state called the dying ReLU problem. This problem can cause several neurons to die and not respond, making set of network passive.


## 5.Leaky ReLU

$$output \ \ A(X) = {{ max(0.01x, x) }}$$


$$output \ f(x) =  \begin{cases}
  \displaystyle 0.01x \ \ \ \ \ \ \ for\     \ x < 0 \\\\
	
  \displaystyle x   \ \ \ \ \ \ \ for\     \ x \ge 0
  \end{cases}$$
	
	
![IMAGE ALT LEAKY ReLU](https://cdn-images-1.medium.com/max/1600/1*LXlJ4zDmYGg9yymgFzyOdA.png)


This is variation of ReLU, which helps mitigating the problem by horizontal line into non-horizontal component.

##### There are other vaiations of ReLU
1. Parameteric rectified linear unit 
2. Randomized leaky rectified linear unit 
3. Exponential linear unit


# How to create an account on GitHub and upload a sample project

## The most basic steps you need to fallow
1.Create a github account.
2.Login into your github account.
3.Click on the [New Repository](https://github.com/new) button.
4.Enter repository name.
5.Click on "Create repository".
> Copy the ```ssh link``` or ```https link```
 we will be using this link for mapping your remote repository with your local repository.


Now you have a created git repository.


## 1. Steps for New Repository from the scratch
### In your local machine.
### Step 1: Installing Git

```shell
sudo apt-get install git # for ubuntu
brew install git # for Mac
```

Download git for Windows [Download Git](https://git-scm.com/downloads)

### Step 2: Configuring Git

```shell
git config --global user.name "<< user name >>"
git config --global user.email "<< user email >>"
```

> `user name ` and `user email` are the github username and useremail.


### Step 2: Creating a project
1. Create a directory, which contains your project.
```shell
mkdir my-project
```

2. Go to the new directory
```shell
cd my-project
```
3. Write your code.
4. Intialize a git local repository.
```shell
git init
```
> Now your git local repo is created. You ca see a hidden file added to your directory(folder). To check ```shell ls -a```.
> You will find .git directory.


5. Map your local branch to your remote branch you have created in git.
```shell 
git remote add origin <remote_name> <remote_repo_url>
``` 
> This above command we use to set an upstream branch for your local branches.

6. Add your all modified files to local staging area
```shell 
git add .
```

> You can use options ``` -A ``` for all files or ``` -u ``` for tracked files instead of ```. ```. Check ``` git help commit ```.
7. Save your changes to your local repository by
```shell
git commit -m "<< commit message >>"
```

> You can use different options as requirement instead of ``` -m ```, check ``` git help commit ```.

8. Save your all changes to remote repository
```shell
git push origin master
```

> ``` push ``` takes varies parameters, to know clear better idea about ``` push ``` command, check ``` git help push```.

9. Go to your github account, and check your latest changes are saved in your remote repository.
 
 10. If you already have a project built and you want to make it as a git repository, then fallow `The most basic steps you need to fallow` till the repository creation and copy the git url(`ssh` or `https` ).
 11. Goto your project and clone it with your old project.

```shell
	git clone <git url>
```

12. Fallow the stps 6,7,8 and 9.
13. Check your git repo it will be updated with your all current project files.
14. If you want bring a remote repository to your local, copy the `ssh` or `https` url and run the fallowing command.
```shell
git clone <git url>
```

