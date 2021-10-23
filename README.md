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


####  Photo gallery grids

####   Animation website grid



