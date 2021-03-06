##  GRIDS
####  Basic grids
> .grid-container{
> display:grid;
  gap:1rem;
}




- > 1- grid with all its columns specified - 1fr=100%, not responsive
> grid-template-columns:1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr 1fr;

- >2- use CSS helper fn - cleaner, repeat(number of columns, size) 
>grid-template-columns: repeat(12, 1fr);
    
- >3- better sizing but overflows horizontally,repeat(no of columns, minmax(size that can't be exceeded, size of each column) ) 
>grid-template-columns: repeat(12, minmax(240px, 1fr));


> - >4- to avoid overflowing on horizontal axis, use Implicit grid
> - >let the algorithm figure out cols / rows
> - >instead of repeating with 12 columns, use auto-fit and minmax

>grid-template-columns:repeat(auto-fit, minmax(240px, 1fr));


#### Responsive mosaic Photo gallery grids.
- some photos are bigger, some taller, wider

- images reposition themselves well as screen reduces

> - NB: 
> If you want images to be all responsive abd the same height, set `grid-auto-rows:"240px"`

> - ` The css code`
> 
> `.grid-images{`
> 
> `display:grid;`
> 
>` grid-template-columns:repeat(auto-fit, minmax(240px, 1fr));`
> 
> `grid-auto-row:240px;`  // same height for all images
> 
> `}`


> To make longer images (longer height)
> Use ` grid-row: span 2;`

> e.g.
>  
> `.card-tall {`
> 
> `grid-row: span 2;`
> 
> `}`


> - Or can use:- `/`  to specify the end point.

> e.g.  `grid-row: span start / end;`  or  `grid-row: start / end;`
>
> `.card-tall{`
>
> `grid-row: span 2 / auto;`
> 
> `}`
>  
> - To make images wider (big width)
> Use `grid-column`
>
> -e.g.
>  `.card-wide{`
> 
> `grid-column: span 2 / auto;`
> 
>`}`
>
> - ` The problem with making images long and wide, such grids don't work on small phones`
> 
> ` The solution is to wrap the classes with long and wide in media queriea `
>
> #### Use Media queries
> ` @media screen and (min-width: 600px) {`
> 
> `.card-tall:{grid-row: span 2 / auto}`
>
> `.card-wide:{grid-column: span 2 / auto}`
> 
> `}`
>












####   Animation website grid



