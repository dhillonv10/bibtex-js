# bibtex-js
The original work for Bibtex-js was done by Henrik Muehe. I am just porting the code and making a few changes to it. 

# Usage

Import jquery:

    <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.4.2/jquery.min.js"></script>

Import the parser:

    <script type="text/javascript" src="https://raw.githubusercontent.com/dhillonv10/bibtex-js/master/bibtex_js.js"></script>
    
    
The bibtex file goes within a textarea tag as follows: 

    <textarea id="bibtex_input" style="display:none;">
    @article{parr1995antlr,
        title={{ANTLR: A predicated-LL (k) parser generator}},
        author={Parr, T.J. and Quong, R.W.},
        journal={Software-Practice and Experience},
        volume={25},
        number={7},
        pages={789--810},
        year={1995},
        publisher={Citeseer}
      }
    </textarea>

The bibliography itself is displayed within a bibtex_display div tag:

    <div id="bibtex_display"></div>

Styling the display can be done as follows:

    <div class="bibtex_template">
        <ul>
            <li style="list-style: none"><span class="if author"></span></li>
            <li>
                <span class="if author"><span class="author" style="font-weight: bold;"></span></span> 
                
                <span class="if year">(<span class="year"></span>)</span> 
                
                <span class="if url" style="margin-left: 20px"><a class="url" style="color:black; font-size:10px">(view online)</a></span>
                
                <span class="if publisher" style="font-weight: bold;"><span class="publisher"></span></span>
                
                <div style="margin-left: 10px; margin-bottom:5px;">
                    <span class="title"></span>
                </div>
                
            </li>
        </ul>
    </div>
