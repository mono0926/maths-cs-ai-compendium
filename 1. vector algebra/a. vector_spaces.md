# Vector Spaces

## Intuition 
Linear algebra is the study of vectors, vector spaces and mappings between vectors.
When you hear "vector," you probably think of an arrow with a direction and magnitude. 
That is the most common example, but in a vector space, a "vector" can be anything: an arrow, a function, a polynomial, anything!
Vector space is just a mathematical "sandbox" with a very specific, unbreakable set of rules:

- **Vector Addition (Combining)**: 
You can take any two vectors and combine them to create a new one. 
Think of vectors as instructions for movement. 
If vector A means "walk 3 steps forward" and vector B means "walk 2 steps right," 
adding them (A + B) creates a new, single instruction: "walk 3 steps forward and 2 steps right."

- **Scalar Multiplication (Scaling)**: 
You can take any vector and scale it using a regular number (a "scalar"). 
You can stretch it, shrink it, or reverse it. 
If vector A is "walk 3 steps forward," scaling it by 2 makes it "walk 6 steps forward." 
Scaling it by -1 flips it entirely to "walk 3 steps backward."

For geometric intuition in machine learning, we will always think of vectors as coordinates in Euclidean space.
For example:

$$\mathbf{a} = [a_1, a_2, a_3, \dots, a_n]$$

the vector $\mathbf{a}$ (denoted mathematically as lowercase letters in bold)
has $n$ coordinates, each representing a position along an axis.

We can for instance represent any object, say, a human, as a vector:

$$\mathbf{h} = [185, 75, 30, 44]$$

where $h_1$ = height in cm, $h_2$ = weight in kg, $h_3$ = age, $h_4$ = waist size in cm.

We can add more features, creating a rich representation of a human, often called feature vectors in ML. 
In ML, vectors are typically high-dimensional, but we can visualise and perform linear algebra on them.
Here is the idea in 3D: 

<svg width="300" height="280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arrow-ax" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#999"/>
    </marker>
    <marker id="arrow-vec" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#e74c3c"/>
    </marker>
  </defs>
  <!-- x-axis -->
  <line x1="140" y1="200" x2="40" y2="250" stroke="#999" stroke-width="1.5" marker-end="url(#arrow-ax)"/>
  <text x="25" y="265" fill="#999" font-size="13" font-style="italic">x</text>
  <!-- y-axis -->
  <line x1="140" y1="200" x2="280" y2="200" stroke="#999" stroke-width="1.5" marker-end="url(#arrow-ax)"/>
  <text x="285" y="205" fill="#999" font-size="13" font-style="italic">y</text>
  <!-- z-axis -->
  <line x1="140" y1="200" x2="140" y2="40" stroke="#999" stroke-width="1.5" marker-end="url(#arrow-ax)"/>
  <text x="145" y="35" fill="#999" font-size="13" font-style="italic">z</text>
  <!-- dashed projections -->
  <line x1="140" y1="200" x2="100" y2="220" stroke="#ccc" stroke-width="1" stroke-dasharray="4,3"/>
  <line x1="100" y1="220" x2="190" y2="220" stroke="#ccc" stroke-width="1" stroke-dasharray="4,3"/>
  <line x1="140" y1="200" x2="230" y2="200" stroke="#ccc" stroke-width="1" stroke-dasharray="4,3"/>
  <line x1="230" y1="200" x2="190" y2="220" stroke="#ccc" stroke-width="1" stroke-dasharray="4,3"/>
  <line x1="190" y1="220" x2="190" y2="100" stroke="#ccc" stroke-width="1" stroke-dasharray="4,3"/>
  <!-- vector a -->
  <line x1="140" y1="200" x2="190" y2="100" stroke="#e74c3c" stroke-width="2.5" marker-end="url(#arrow-vec)"/>
  <!-- point -->
  <circle cx="190" cy="100" r="4" fill="#e74c3c"/>
  <!-- label -->
  <text x="198" y="95" fill="#e74c3c" font-size="14" font-weight="bold">a = (3, 2, 4)</text>
  <!-- origin -->
  <circle cx="140" cy="200" r="3" fill="#333"/>
  <text x="145" y="215" fill="#333" font-size="12">O</text>
</svg>

## Vector Addition

- Vector addition can be performed by placing one vector on the tail of the other visually, and drawing from the origin to the endpoint.

<svg width="400" height="200" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arrow-a" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#e74c3c"/>
    </marker>
    <marker id="arrow-b" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#3498db"/>
    </marker>
    <marker id="arrow-sum" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#2ecc71"/>
    </marker>
  </defs>
  <!-- a vector -->
  <line x1="40" y1="160" x2="168" y2="160" stroke="#e74c3c" stroke-width="2.5" marker-end="url(#arrow-a)"/>
  <text x="100" y="180" fill="#e74c3c" font-size="14" font-weight="bold" text-anchor="middle">a</text>
  <!-- b vector from tip of a -->
  <line x1="176" y1="160" x2="256" y2="60" stroke="#3498db" stroke-width="2.5" marker-end="url(#arrow-b)"/>
  <text x="230" y="100" fill="#3498db" font-size="14" font-weight="bold">b</text>
  <!-- a + b resultant -->
  <line x1="40" y1="160" x2="256" y2="60" stroke="#2ecc71" stroke-width="2.5" stroke-dasharray="6,3" marker-end="url(#arrow-sum)"/>
  <text x="130" y="95" fill="#2ecc71" font-size="14" font-weight="bold">a + b</text>
  <!-- origin label -->
  <circle cx="40" cy="160" r="3" fill="#333"/>
  <text x="28" y="178" fill="#333" font-size="12">O</text>
</svg>

- For two vectors $\mathbf{a} = (a_1, a_2)$ and $\mathbf{b} = (b_1, b_2)$: $\mathbf{a} + \mathbf{b} = (a_1 + b_1, a_2 + b_2)$
- Vectors can also be subtracted, with all addition rules applying too.

## Scalar Multiplication

- Multiplying a vector by a scalar scales the vector by that factor in the same direction.

<svg width="420" height="120" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arrow-v" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#e74c3c"/>
    </marker>
    <marker id="arrow-2v" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#3498db"/>
    </marker>
    <marker id="arrow-neg" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#9b59b6"/>
    </marker>
  </defs>
  <!-- v -->
  <line x1="20" y1="50" x2="88" y2="50" stroke="#e74c3c" stroke-width="2.5" marker-end="url(#arrow-v)"/>
  <text x="50" y="40" fill="#e74c3c" font-size="14" font-weight="bold">v</text>
  <circle cx="20" cy="50" r="3" fill="#333"/>
  <!-- 2v -->
  <line x1="140" y1="50" x2="278" y2="50" stroke="#3498db" stroke-width="2.5" marker-end="url(#arrow-2v)"/>
  <text x="200" y="40" fill="#3498db" font-size="14" font-weight="bold">2v</text>
  <circle cx="140" cy="50" r="3" fill="#333"/>
  <!-- -v -->
  <line x1="380" y1="50" x2="312" y2="50" stroke="#9b59b6" stroke-width="2.5" marker-end="url(#arrow-neg)"/>
  <text x="340" y="40" fill="#9b59b6" font-size="14" font-weight="bold">-v</text>
  <circle cx="380" cy="50" r="3" fill="#333"/>
  <!-- labels -->
  <text x="20" y="90" fill="#666" font-size="12">original</text>
  <text x="155" y="90" fill="#666" font-size="12">scaled (2x)</text>
  <text x="315" y="90" fill="#666" font-size="12">negated</text>
</svg>

- For a scalar $c$ and vector $\mathbf{v} = (v_1, v_2)$: $c\mathbf{v} = (cv_1, cv_2)$

## Closure under Addition

- If you add any two vectors from the vector space, the result is also a vector within the same space: If $\mathbf{u} \in V$ and $\mathbf{v} \in V$, then $\mathbf{u} + \mathbf{v} \in V$

## Closure under Scalar Multiplication

- If you multiply any vector from the vector space by a scalar, the result is a vector within the same space: If $\mathbf{v} \in V$ and $c \in F$, then $c\mathbf{v} \in V$

## Associativity of Addition

- For any three vectors $\mathbf{u}$, $\mathbf{v}$, and $\mathbf{w}$: $(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})$

## Commutativity of Addition

- For any two vectors $\mathbf{u}$ and $\mathbf{v}$: $\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$

<svg width="300" height="220" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arrow-cu" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#e74c3c"/>
    </marker>
    <marker id="arrow-cv" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#3498db"/>
    </marker>
    <marker id="arrow-cs" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#2ecc71"/>
    </marker>
  </defs>
  <!-- u from origin -->
  <line x1="30" y1="180" x2="198" y2="180" stroke="#e74c3c" stroke-width="2.5" marker-end="url(#arrow-cu)"/>
  <text x="110" y="200" fill="#e74c3c" font-size="14" font-weight="bold" text-anchor="middle">u</text>
  <!-- v from origin -->
  <line x1="30" y1="180" x2="110" y2="60" stroke="#3498db" stroke-width="2.5" marker-end="url(#arrow-cv)"/>
  <text x="55" y="115" fill="#3498db" font-size="14" font-weight="bold">v</text>
  <!-- v from tip of u (dashed) -->
  <line x1="206" y1="180" x2="270" y2="60" stroke="#3498db" stroke-width="1.5" stroke-dasharray="5,3" marker-end="url(#arrow-cv)"/>
  <!-- u from tip of v (dashed) -->
  <line x1="118" y1="60" x2="270" y2="60" stroke="#e74c3c" stroke-width="1.5" stroke-dasharray="5,3" marker-end="url(#arrow-cu)"/>
  <!-- resultant diagonal -->
  <line x1="30" y1="180" x2="270" y2="60" stroke="#2ecc71" stroke-width="2" stroke-dasharray="6,3" marker-end="url(#arrow-cs)"/>
  <text x="165" y="105" fill="#2ecc71" font-size="14" font-weight="bold">u + v</text>
  <!-- origin -->
  <circle cx="30" cy="180" r="3" fill="#333"/>
  <text x="18" y="198" fill="#333" font-size="12">O</text>
</svg>

- Both paths through the parallelogram arrive at the same point.

## Existence of Additive Identity (Zero Vector)

- There exists a vector $\mathbf{0}$ such that for any vector $\mathbf{v}$: $\mathbf{v} + \mathbf{0} = \mathbf{v}$

<svg width="300" height="100" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arrow-id" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#e74c3c"/>
    </marker>
  </defs>
  <line x1="30" y1="45" x2="118" y2="45" stroke="#e74c3c" stroke-width="2.5" marker-end="url(#arrow-id)"/>
  <text x="70" y="35" fill="#e74c3c" font-size="14" font-weight="bold" text-anchor="middle">v</text>
  <circle cx="30" cy="45" r="3" fill="#333"/>
  <text x="145" y="50" fill="#333" font-size="18">+</text>
  <circle cx="175" cy="45" r="4" fill="#999"/>
  <text x="175" y="75" fill="#999" font-size="12" text-anchor="middle">0</text>
  <text x="200" y="50" fill="#333" font-size="18">=</text>
  <line x1="220" y1="45" x2="288" y2="45" stroke="#e74c3c" stroke-width="2.5" marker-end="url(#arrow-id)"/>
  <text x="254" y="35" fill="#e74c3c" font-size="14" font-weight="bold" text-anchor="middle">v</text>
  <circle cx="220" cy="45" r="3" fill="#333"/>
</svg>

## Existence of Additive Inverse

- For every vector $\mathbf{v}$, there exists a vector $-\mathbf{v}$ such that: $\mathbf{v} + (-\mathbf{v}) = \mathbf{0}$

<svg width="320" height="100" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arrow-inv-v" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#e74c3c"/>
    </marker>
    <marker id="arrow-inv-neg" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#3498db"/>
    </marker>
  </defs>
  <!-- v going right -->
  <line x1="30" y1="45" x2="118" y2="45" stroke="#e74c3c" stroke-width="2.5" marker-end="url(#arrow-inv-v)"/>
  <text x="75" y="35" fill="#e74c3c" font-size="14" font-weight="bold" text-anchor="middle">v</text>
  <!-- -v going back left from tip of v -->
  <line x1="126" y1="45" x2="38" y2="45" stroke="#3498db" stroke-width="2.5" marker-end="url(#arrow-inv-neg)"/>
  <text x="85" y="70" fill="#3498db" font-size="14" font-weight="bold" text-anchor="middle">-v</text>
  <circle cx="30" cy="45" r="3" fill="#333"/>
  <!-- equals zero -->
  <text x="155" y="50" fill="#333" font-size="18">=</text>
  <circle cx="195" cy="45" r="5" fill="#999"/>
  <text x="195" y="75" fill="#999" font-size="14" font-weight="bold" text-anchor="middle">0</text>
</svg>

## Distributivity of Scalar Multiplication over Vector Addition

- For any scalar $c$ and vectors $\mathbf{u}$, $\mathbf{v}$: $c(\mathbf{u} + \mathbf{v}) = c\mathbf{u} + c\mathbf{v}$

<svg width="360" height="220" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <marker id="arrow-du" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#e74c3c"/>
    </marker>
    <marker id="arrow-dv" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#3498db"/>
    </marker>
    <marker id="arrow-ds" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#2ecc71"/>
    </marker>
    <marker id="arrow-dc" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <path d="M0,0 L8,3 L0,6" fill="#f39c12"/>
    </marker>
  </defs>
  <!-- original u (short) -->
  <line x1="30" y1="190" x2="98" y2="190" stroke="#e74c3c" stroke-width="2" marker-end="url(#arrow-du)"/>
  <text x="60" y="208" fill="#e74c3c" font-size="12" font-weight="bold" text-anchor="middle">u</text>
  <!-- original v from tip of u (short) -->
  <line x1="106" y1="190" x2="146" y2="140" stroke="#3498db" stroke-width="2" marker-end="url(#arrow-dv)"/>
  <text x="137" y="172" fill="#3498db" font-size="12" font-weight="bold">v</text>
  <!-- u+v resultant (short) -->
  <line x1="30" y1="190" x2="146" y2="140" stroke="#2ecc71" stroke-width="1.5" stroke-dasharray="4,3" marker-end="url(#arrow-ds)"/>
  <text x="72" y="155" fill="#2ecc71" font-size="11">u+v</text>
  <!-- scaled: cu (long) -->
  <line x1="30" y1="190" x2="166" y2="190" stroke="#e74c3c" stroke-width="2.5" marker-end="url(#arrow-du)"/>
  <!-- scaled: cv from tip of cu -->
  <line x1="174" y1="190" x2="254" y2="90" stroke="#3498db" stroke-width="2.5" marker-end="url(#arrow-dv)"/>
  <!-- c(u+v) resultant (long, gold) -->
  <line x1="30" y1="190" x2="254" y2="90" stroke="#f39c12" stroke-width="2.5" stroke-dasharray="6,3" marker-end="url(#arrow-dc)"/>
  <text x="160" y="115" fill="#f39c12" font-size="14" font-weight="bold">c(u + v)</text>
  <!-- labels -->
  <text x="95" y="185" fill="#e74c3c" font-size="12" font-weight="bold">cu</text>
  <text x="225" y="130" fill="#3498db" font-size="12" font-weight="bold">cv</text>
  <!-- origin -->
  <circle cx="30" cy="190" r="3" fill="#333"/>
  <text x="18" y="208" fill="#333" font-size="12">O</text>
</svg>

- Scaling the sum (gold) gives the same result as summing the scaled vectors.

## Distributivity of Scalar Multiplication over Scalar Addition

- For any scalars $c$, $d$ and vector $\mathbf{v}$: $(c + d)\mathbf{v} = c\mathbf{v} + d\mathbf{v}$

## Associativity of Scalar Multiplication

- For any scalars $c$, $d$ and vector $\mathbf{v}$: $(cd)\mathbf{v} = c(d\mathbf{v})$

## Identity Element of Scalar Multiplication

- For any vector $\mathbf{v}$: $1\mathbf{v} = \mathbf{v}$, where $1$ is the multiplicative identity in the field of scalars.
