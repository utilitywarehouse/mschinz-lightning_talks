- title : dotnet core
- description : State of affairs with dotnet core
- author : Martin Schinz
- theme : beige
- transition : default

***

## dotnet core

- what is it?
- why would i want to use it?
- what are the problems

***

### what is dotnet core?

' &darr; for what is dotnet
' &rarr; for what is core


---

### What is dotnet?


<section>
<ul>
<li class="fragment">Microsoft Technology</li>
<li class="fragment">FCL (Framework Class Library)</li>
<li class="fragment">CLR (Comman Language Runtime)</li>
<li class="fragment">Oftentimes mistakenly used as another word for C#</li>
<li class="fragment">Especially by recruiters</li>
<li style="list-style-type: none" class="fragment"><img src="images/moron2.gif" alt="moron" title="recruiter" style="float: left"/></li>
</ul>
</section>

' garbage collector
' jvm
' better java
' traditionally problems with x-plat

***

### dotnet core is

- all of normal dotnet ('ish)
- x-platform
- single binary (embedded vm) platform target

***

### i would use it when

<section>
<ul>
<li class="fragment">I want / need to run on linux</li>
<li class="fragment">I want /need to run on docker</li>
<li class="fragment">I want to preserve current business code, but upgrade surrounding technology</li>
</section>

---

#### or I find masochist pleasure in following microsoft's alpha release channel


<img style="width: 600px" src="images/tennisballs.gif" alt="tennis balls" title="Micorosoft's alpha channel"/>


_It feels like there are a lot of developers at Microsoft_

***

### what are the problems

- Speed of evolution
- Maturity of surrounding ecosystem / tooling
- Anxiety of community to adopt / 3d party libs


***

### my crystal ball tells me....

![crystal_ball](images/crystal_ball.jpeg) <!-- .element: style="width: 200px" -->

---

### dotnet core will

- strengthen Microsoft's efforts to stay relevant in the server market, but not neccessarily using windows
- will be in a good place to integrate with hypervisors. Unikernels are a _thing_
- be adopted by companies using windows technologies as their current development platform

---

### dotnet core will not

- become a relevant technology choice for companies currently invested in languages running on unix platforms
- replace most windows deployments
- become a _hipster_ web development tool

