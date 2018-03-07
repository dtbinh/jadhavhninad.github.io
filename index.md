---
layout: default
---

Text can be **bold**, _italic_, ~~strikethrough~~ or `keyword`.

# [](#header-1)Neural Network Classifier for MNIST DataSet
[Link to Github Repo](https://github.com/jadhavhninad/Neural-Network-Classifier-for-MNIST-DataSet).

### [](#header-3) Goals:
To implement a two layer neural network for a binary classifier and a multi layer neural network for a multiclass classifier. Compare performance with K-Nearest Neighbour approach for same dataset size.

### [](#header-3) Implementation:
*   The two layer network has 1 hidden layer dimension=500, for binary classification. The multilayer neural network program is able to create and train a multilayer network based on command line arguments. 
*   Two approaches for K-Nearest Neighbour have been tried - using the default python package and building the algorithm from scratch. 
*   Since the MNIST dataset has 60,000 images which is too large for batch gradient descent. Therefore, training is done with 6000 samples and test with 1000 samples.

### [](#header-3) Output:
*   The training and testing accuracies. 
*   Plot of train error vs iterations
*   Plot of K-value vs Error (for kNN)


## [](#header-1)Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### [](#header-3)Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### [](#header-4)Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### [](#header-5)Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### [](#header-6)Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image

![](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
