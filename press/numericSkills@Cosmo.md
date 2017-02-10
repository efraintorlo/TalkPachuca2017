---
author: Efrain Torres
title: Cosmo @ Pachuca 17
---
= data-x="0"

On the numeric life in Cosmology
==================================================================

## The open-source software in Science

```c++
Talk Pachuca;
Pachuca.place = "ICBI@UAEH";
Pachuca.date = "Feb 2017";
Pachuca.repo = "https://github.com/elchinot7/TalkPachuca2017";
```

```python
credentials = {
                "author": "Efrain Torres",
                "e-mail": "efrain@fisica.ugto.mx",
                "institution": "Universidad de Guanajuato",
              }
```

---
= data-x="1000"


# Resumen

## 1. Numeric life at Science
## 2. Cosmology: Supernavae `Python`
## 3. Particle Phyisics: `Python` and `C++`

---
= data-x="2000"

# Programming Skills in science

<div class="row">

    <div class='col-md-10 col-md-offset-0'>
<img src="./img/img/figures/code_quality/code_quality.png" alt="Image1" style="width:1000px;height:300px;">
    </div>
 </br>

</div>
[https://arxiv.org/abs/1507.03989](https://arxiv.org/abs/1507.03989)

---
= data-x='3000', data-y='000', data-z='000'

## Are we trained?

<img src="./img/img/figures/are_we_trained4/are_we_trained.png" alt="HTML5-IMAGE" style="width:1200px;height:240px;">
<img src="./img/img/figures/training_by_country2/training_by_country.png" alt="HTML5-IMAGE" style="width:900px;height:450px;">


---
= data-x='4000', data-y='000', data-z='000'

## Tools

<img src="./img/img/figures/tools_by_career1/tools_by_career.png" alt="HTML5-IMAGE" style="width:1200px;height:600px;">

---
= data-x='5000', data-y='000', data-z='000'

# Numeric stuff is hard

### From the SNANA Legal Team:

[http://snana.uchicago.edu/doc/snana_legal_notice.pdf](http://snana.uchicago.edu/doc/snana_legal_notice.pdf)

### SIDE EFFECTS include, but are not limited to:

- Confusion, frustration, watery eyes, headaches, weight loss, weight gain,
systematics-limited results, incorrect results, denial of tenure.

- Do not drive or operate heavy machinery while using SNANA.



---
= data-x="6000"


<div class="row">

<div class='col-md-4 col-md-offset-0'>
<h2> Programming Languages</h2>
<pre><code class='prettyprint Bash' style='line-height: 25px;'>Languages/
│ 
├── Compiled
│   ├── Java
│   ├── Fortran
│   ├── Pascal
│   ├── C
│   ├── C++
│   ├── C#
│   └── Go
│ 
├─── Scripting
│    ├── Perl
│    ├── JavaScript
│    ├── Swift
│    └── Python
│   
└── Databases
    ├── SQL
    ├── MySQL
    ├── SQLite
    └── PostgreSQL
</code></pre>
</div>

 <div class='col-md-5 col-md-offset-1'>
 <h2> In Physics...</h2>
<pre><code class='prettyprint Bash' style='line-height: 25px;'>Codes/
│ 
├── Cosmo
│   ├── CosmoMC (Fortran 2008)
│   ├── Class (C++)
│   ├── Astropy (Python)
│   ├── MontePython (Python)
│   ├── SciKit-learn (Python)
│   └── Cosmosis (Framework)
│ 
├── High-Energy
│   ├── ROOT (C++)
│   ├── PyROOT (Python wraper)
│   └─  POW (Fortan)
│ 
└── Databases
    ├── SQL
    ├── *.fits
    └── *.root
</code></pre>
</div>

</div>

---
= data-x="7000"


## The advisors use to ask simple things as:
</br>

### **Can you solve this set of equations for tomorrow?**
</br>
### **Plot this solution and send me the figure.**


---
= data-x='6000', data-y='0', data-z='1000'


<div class="row">

    <div class='col-md-10 col-md-offset-0'>
		<img src="./img/img/mathematica_pricing.png" alt="Image1" style="width:1000px;height:700px;">
    </div>

</div>

---
= data-x='7000', data-y='0', data-z='0000'


<div class="row">

    <div class='col-md-10 col-md-offset-0'>
		<img src="./img/img/maple_pricing.png" alt="Image1" style="width:1000px;height:700px;">
    </div>

</div>


---
= data-x='8000', data-y='0', data-z='000'


<div class="row">

    <div class='col-md-10 col-md-offset-0'>
		<img src="./img/img/matlab_pricing.png" alt="Image1" style="width:1000px;height:700px;">
    </div>

</div>

---
= data-x='9000', data-y='0', data-z='00'

<div class="row">

    <div class='col-md-5 col-md-offset-0'>
    <img src="./img/img/c++_hard_meme.jpg" alt="Image1" style="width:600px;height:700px;">
    </div>
    <div class='col-md-5 col-md-offset-2'>
    </br>
    </br>
        <img src="./img/img/c_vs_python_tshirt.jpg" alt="Image1" style="width:400px;height:400px;">
    </div>

</div>


---
= data-x='10000', data-y='0', data-z='00'

# ` C++` vs ` Python`

## `C++`

```c++
#include &lt;iostream.h&gt;

void main()
{
cout << "Hello world" << endl;
}
```


## `Python`

```{python}
print("Hello World")
```

---
= data-x='11000', data-y='000', data-z='000'

## Cuda

<pre><code class='prettyprint C ' style='font-size: 15px !important; line-height: 18px;'>#include &lt;stdio.h&gt;
const int N = 16;
const int blocksize = 16;

 &#95;&#95;global&#95;&#95; </br>
void hello(char *a, int *b)
{
	a[threadIdx.x] += b[threadIdx.x];
}

int main()
{
	char a[N] = "Hello \0\0\0\0\0\0";
	int b[N] = {15, 10, 6, 0, -11, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0};
	char *ad;
	int *bd;
	const int csize = N*sizeof(char);
	const int isize = N*sizeof(int);

	printf("%s", a);

	cudaMalloc( (void**)&ad, csize );
	cudaMalloc( (void**)&bd, isize );
	cudaMemcpy( ad, a, csize, cudaMemcpyHostToDevice );
	cudaMemcpy( bd, b, isize, cudaMemcpyHostToDevice );
	dim3 dimBlock( blocksize, 1 );
	dim3 dimGrid( 1, 1 );
	hello&lt;&lt;&lt;dimGrid, dimBlock&gt;&gt;&gt;(ad, bd);
	cudaMemcpy( a, ad, csize, cudaMemcpyDeviceToHost );
	cudaFree( ad );
	cudaFree( bd );
	printf("%s\n", a);
	return EXIT_SUCCESS;
}
</code></pre>



---
= data-x='12000', data-y='000', data-z='000'

<img src="./img/img/stroustrup_confused.png" alt="HTML5-IMAGE" style="width:1000px;height:700px;">





---
= data-x='13000', data-y='000', data-z='000'

# TITLE


## [Example 1](../InflationExample/index_local.html#/step-2)




---
= data-x '13000', data-y='0', data-z='-100'

# Jobs

<img src="./img/img/glassdoor_data_scientist_job.png" alt="HTML5-IMAGE" style="width:1200px;height:600px;">


- [https://www.linkedin.com/jobs/view/122233571](https://www.linkedin.com/jobs/view/122233571)
