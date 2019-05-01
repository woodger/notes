Given an array a that contains only numbers in the range from 1 to a.length, find the first duplicate number for which the second occurrence has the minimal index. In other words, if there are more than 1 duplicated numbers, return the number for which the second occurrence has a smaller index than the second occurrence of the other number does. If there are no such elements, return -1.

Example

For a = [2, 1, 3, 5, 3, 2], the output should be firstDuplicate(a) = 3.

There are 2 duplicates: numbers 2 and 3. The second occurrence of 3 has a smaller index than the second occurrence of 2 does, so the answer is 3.

For a = [2, 2], the output should be firstDuplicate(a) = 2;

For a = [2, 4, 3, 5, 1], the output should be firstDuplicate(a) = -1.

Input/Output

[execution time limit] 4 seconds (js)

[input] array.integer a

Guaranteed constraints:
1 ≤ a.length ≤ 105,
1 ≤ a[i] ≤ a.length.

[output] integer

The element in a that occurs in the array more than once and has the minimal index for its second occurrence. If there are no such elements, return -1.
[JavaScript (ES6)] Syntax Tips

// Prints help message to the console
// Returns a string
function helloWorld(name) {
    console.log("This prints to the console when you Run Tests");
    return "Hello, " + name;
}

****

You are given a list dishes, where each element consists of a list of strings beginning with the name of the dish, followed by all the ingredients used in preparing it. You want to group the dishes by ingredients, so that for each ingredient you'll be able to find all the dishes that contain it (if there are at least 2 such dishes).

Return an array where each element is a list beginning with the ingredient name, followed by the names of all the dishes that contain this ingredient. The dishes inside each list should be sorted lexicographically, and the result array should be sorted lexicographically by the names of the ingredients.

Example

For
  dishes = [["Salad", "Tomato", "Cucumber", "Salad", "Sauce"],
            ["Pizza", "Tomato", "Sausage", "Sauce", "Dough"],
            ["Quesadilla", "Chicken", "Cheese", "Sauce"],
            ["Sandwich", "Salad", "Bread", "Tomato", "Cheese"]]
the output should be
  groupingDishes(dishes) = [["Cheese", "Quesadilla", "Sandwich"],
                            ["Salad", "Salad", "Sandwich"],
                            ["Sauce", "Pizza", "Quesadilla", "Salad"],
                            ["Tomato", "Pizza", "Salad", "Sandwich"]]
For
  dishes = [["Pasta", "Tomato Sauce", "Onions", "Garlic"],
            ["Chicken Curry", "Chicken", "Curry Sauce"],
            ["Fried Rice", "Rice", "Onions", "Nuts"],
            ["Salad", "Spinach", "Nuts"],
            ["Sandwich", "Cheese", "Bread"],
            ["Quesadilla", "Chicken", "Cheese"]]
the output should be
  groupingDishes(dishes) = [["Cheese", "Quesadilla", "Sandwich"],
                            ["Chicken", "Chicken Curry", "Quesadilla"],
                            ["Nuts", "Fried Rice", "Salad"],
                            ["Onions", "Fried Rice", "Pasta"]]
Input/Output

[execution time limit] 4 seconds (js)

[input] array.array.string dishes

An array of dishes, where dishes[i] for each valid i contains information about the ith dish: dishes[i][0] is the name of the dish, and all the elements after it are the ingredients of that dish. Both the dish name and the ingredient names consist of English letters and spaces. It is guaranteed that all dish names are different. It is also guaranteed that the ingredient names for any one dish are also pairwise distinct.

Guaranteed constraints:
1 ≤ dishes.length ≤ 500,
2 ≤ dishes[i].length ≤ 10,
1 ≤ dishes[i][j].length ≤ 50.

[output] array.array.string

The array containing the grouped dishes.
[JavaScript (ES6)] Syntax Tips

// Prints help message to the console
// Returns a string
function helloWorld(name) {
    console.log("This prints to the console when you Run Tests");
    return "Hello, " + name;
}

47
129


****

Note: Try to solve this task in O(m + n) or O(n) time, where n is a number of vertices and m is a number of edges, since this is what you'll be asked to do during an interview.

In a multithreaded environment, it's possible that different processes will need to use the same resource. A wait-for graph represents the different processes as nodes in a directed graph, where an edge from node i to node j means that the node j is using a resource that node i needs to use (and cannot use until node j releases it).

We are interested in whether or not this digraph has any cycles in it. If it does, it is possible for the system to get into a state where no process can complete.

We will represent the processes by integers 0, ...., n - 1. We represent the edges using a two-dimensional list connections. If j is in the list connections[i], then there is a directed edge from process i to process j.

Write a function that returns True if connections describes a graph with a directed cycle, or False otherwise.

Example

For connections = [[1], [2], [3, 4], [4], [0]], the output should be
hasDeadlock(connections) = true.


This graph contains a cycle.

For connections = [[1, 2, 3], [2, 3], [3], []], the output should be
hasDeadlock(connections) = false.


This graph doesn't contain a directed cycle (there are two paths from 0 to 3, but no paths from 3 back to 0).

Input/Output

[execution time limit] 4 seconds (js)

[input] array.array.integer connections

A representation of the graphs edges. connection.length is the number of vertices. If j is in the list connections[i], then there is a directed edge from process i to process j.

Guaranteed constraints:
1 ≤ connections.length ≤ 500,
0 ≤ connections[i][j] < connections.length,
connections[i][j] ≠ connections[i][k] for j ≠ k,
i not in connections[i].

[output] boolean

Return True if connections describes a graph with a directed cycle, or False otherwise.
[JavaScript (ES6)] Syntax Tips

// Prints help message to the console
// Returns a string
function helloWorld(name) {
    console.log("This prints to the console when you Run Tests");
    return "Hello, " + name;
}

15
0


****

All DNA is composed of a series of nucleotides abbreviated as A, C, G, and T. In research, it can be useful to identify repeated sequences within DNA.

Write a function to find all the 10-letter sequences (substrings) that occur more than once in a DNA molecule s, and return them in lexicographical order. These sequences can overlap.

Example

For s = "AAAAACCCCCAAAAACCCCCCAAAAAGGGTTT", the output should be
repeatedDNASequences(s) = ["AAAAACCCCC", "CCCCCAAAAA"].

Input/Output

[execution time limit] 4 seconds (js)

[input] string s

Guaranteed constraints:
0 ≤ s.length ≤ 5000.

[output] array.string

An array containing all of the potential 10-letter sequences that occur more than once in s.
[JavaScript (ES6)] Syntax Tips

// Prints help message to the console
// Returns a string
function helloWorld(name) {
    console.log("This prints to the console when you Run Tests");
    return "Hello, " + name;
}

5
8



// function firstDuplicate(a) {
//   const buf = [];
//
//   for (let i of a) {
//     if (buf.indexOf(i) > -1) {
//       return i;
//     }
//
//     buf.push(Number(i));
//   }
//
//   return -1;
// }
//
// const res = firstDuplicate([2, 1, 3, 5, 3, 2]);
//
// debugger;

//
// function groupingDishes(dishes) {
//   const hash = {};
//
//   for (let dishe of dishes) {
//     const [name] = dishe;
//
//     for (let i = dishe.length - 1; i > 0; i--) {
//       const comp = dishe[i];
//
//       if (hash[comp] === undefined) {
//         hash[comp] = [];
//       }
//
//       hash[comp].push(name);
//     }
//   }
//
//   const food = [];
//   const keys = Object.keys(hash);
//
//   keys.sort();
//
//   for (let i of keys) {
//     const comp = hash[i];
//
//     if (comp.length > 1) {
//       food.push([i, ...comp]);
//     }
//   }
//
//   return food;
// }
//
// const dishes = [["Salad", "Tomato", "Cucumber", "Salad", "Sauce"],
//             ["Pizza", "Tomato", "Sausage", "Sauce", "Dough"],
//             ["Quesadilla", "Chicken", "Cheese", "Sauce"],
//             ["Sandwich", "Salad", "Bread", "Tomato", "Cheese"]];
//
// const res = groupingDishes(dishes);
// debugger;


function repeatedDNASequences(s) {
  const dna = [];

  for (let i of s) {
    if (dna.length === 0) {
      dna.push([i, 0]);
    }

    let cursor = dna[dna.length - 1];

    if (cursor[0] === i) {
      cursor[1]++;
    }
    else {
      dna.push([i, 1]);
    }
  }

  const sequence = [];

  for (let i = 0; i > dna.length - 1; i++) {
    const pair = [];
    const left = dna[i];
    const right = dna[i + 1];

    sequence.push(left, right);

    // if (left[1] + right[1] > 10) {
    //   sequence.push(left, right);
    // }
  }

  debugger;

  // const res = [];
  //
  // for (let i of dna) {
  //
  // }
}

const res = repeatedDNASequences('AAAAACCCCCAAAAACCCCCCAAAAAGGGTTT');
