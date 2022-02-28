H&M Lite: 172 Hours                                                                                        Stack: Vanilla (HTML, CSS, JS)

Objective: Replicate a Responsive Website 
Purpose: Learn good design practices and test current css knowledge

Hours Worked
• Designing Products and Layouts (4 hours)
• Website (168 hours)


Requirements: 
• Must look 90%+ identical 
• Cannot look at HTML design from source to copy structure *A1

Allowed:
•Copying fonts, colors and sizes (Reasoning: The focus is learning design practices to apply to future projects)
•*A1 Looking at images, understanding div sections breakpoints, and seeing if pseudo elements are used (Reasoning: This helps future functionality and understanding of libraries used (SASS, jQuery, etc)). This can help guide me to the next topics I need to study. 




What's the most technically challenging part of this project and why?
Building a strong foundation for my project was difficult. Whenever I thought a complex div was finished, I realized I missed a few elements or didn’t wrap correctly. This also applied to JS functions. I accepted any answer that worked instead of considering how it’d work with other functions/elements. 
>> This wasted a lot of time and could have been avoided if I spent more time thinking about scalability. Whenever I kept trying to build on top of the base, I’d have to rewrite functionality. 




Realizations: 
• You can use a comma (“,”) for a space when using classList.add
• Pseudo Elements can be Classes or Elements and are used to decorate the page. If an image doesn’t load, a pseudo element can be shown to display an idea of what should be there. It can also be used to save space if elements aren’t used on certain media queries. \
• Using px’s for most elements is acceptable. 
>> This was eye opening because I thought only % and viewport lengths were acceptable unless working on fixed elements (borders). However, the main idea is making the website accessible to everyone. If the element is RWD with PX, it doesn’t matter what measurements are used. 
•  Padding/Max Width’s should be used with CSS Grid’s. This allows more RWD. 
• Hiding/Showing text through buttons can be done to increase user experience. 
• Only some element retrievers are live.  

The difference between HTMLcollection live vs nodelist 

document.getElementsByClassName() is an HTMLCollection, and is live.
document.getElementsByTagName() is an HTMLCollection, and is live.
document.getElementsByName() is a NodeList and is live.
document.querySelectorAll() is a NodeList and is not live.

Lesson Credit | Sasha Kondrashov  https://stackoverflow.com/questions/14377590/queryselector-and-queryselectorall-vs-getelementsbyclassname-and-getelementbyid


Problems:


Major:

•(NA) Not understanding the Entire Scope of the Project |
Not downloading all necessary content  
I had the idea of making H&M Lite for weeks now. I downloaded what I needed for the design but didn't explore what H&M uses. 
There were overlay png's, product names, designs, and other content that changed since I wrote down the idea. Thus, it's hard to get
everything 1:1, particularly the product names and prices. 

• !(1) Dynamic Creation of Custom Filters Stopping |
This issue is replicated by deleting all filters and attempting to readd new filters. 
I’ve spent time trying to understand the error to no avail. The code should work because the new elements can be displayed in the console. 

Root Issue Idea: I think this issue lies with how exclusive filters was functioned or dynamic creation failing due to node value changing after deletion of all filters. 



• (2) Cart Multiplication is Incorrect
     6.99 (Base Product Value - ID 1)
Quantity     	Output                  Expected
(2)              	20.97                     13.98
(3) 	      	 41.94                    20.97
(4)	      	 69.9                      27.96
(5) 	      	 104.85        	      34.95

Solution: Simplifying selectors to only one selector for the total. I used too many selectors and unnecessary computation.


• (3) Exclusive Filter Options  | 
Some Filters can’t coexist, such as Highest Price and Lowest Price. I had a problem being able to filter through all custom filter tags. Whenever I tried to remove a filter, all of them would be removed. 

Solution: Using an indexOf to filter between the custom filters and only deleting tags that fit the criteria. 



• (4) Filtered Searches with more than 1 Word |. 
Huge issue: I didn't think ahead and create a filter system for the products. If I added a div with types, filtering would've been easy, especially colors.

Solution: Order of word filters mattered. If I placed the color filter at the bottom, all products would become hidden. I had to think of execution order of filters and then organize accordingly. 



Minor: 
• Comments lead to line breaks (Only CSS)|

• HTML Collection vs nodeList |
var sizeTest5 = document.querySelectorAll(“div.filtContainer.fav”);
Array.from(sizeTest5).forEach(sideTest5 => sideTest5.classList.add('hideFilterContainer'));

document.querySelectorAll is static, however, I used Array.from to get an updated list and use forEach to cycle to achieve the result I wanted : making all new favorite products hide sizeContainers. 


•  Not Using a Declaration when using For Of Loops
for(let aBtn of addTest){       /*let must be used. Declaration stores variable*/















Future Features: 
• Making Advanced searches (3-7 word searches)
>> With auto-correct searches
• A product grid size change button (red/white buttons on the right side above filter headers)
• Switch sections (Men/Women and even new sections)
• Saving space in the HTML & CSS write up by using a database for products or an alternative solution




