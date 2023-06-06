# duplicateValues
find duplicate and same values in two array  
head>
    
    <title>Duplicate Array</title>
</head>
<body>
    <script>
   var fullWordList = ['1', '2', '3', '4', '5'];
var wordsToRemove = ['1', '2', '3'];

var duplicates = [];
var sameValues = [];

// Find duplicates and same values
for (var i = 0; i < fullWordList.length; i++) {
  var word = fullWordList[i];
  
  if (wordsToRemove.includes(word)) {
    sameValues.push(word);
    
    // Check for duplicates
    if (fullWordList.indexOf(word, i + 1) !== -1) {
      duplicates.push(word);
    }
  }
}

console.log("Duplicates:", duplicates); // Output: ['1', '2', '3']
console.log("Same Values:", sameValues); // Output: ['1', '2', '3']

</script>
    
</body>
</html>
