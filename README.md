Simple Jquery Accordion
=================================

Simple Jquery Accordion is very simple

[Article on jqueryHub](#)

[Demo](#)


How to use
==========

        <div id="demoTab">          
            <ul class="resp-tabs-list">
                <li> .... </li>
                <li> .... </li>
                <li> .... </li>
            </ul> 

            <div class="resp-tabs-container">                                                        
                <div> ....... </div>
                <div> ....... </div>
                <div> ....... </div>
            </div>
        </div>


<pre>
<code>
(function($) {
  $('.sm-accordion-heading.active + .sm-accordion-content').slideDown();
  $('.sm-accordion-heading').click(function(){
    var nextall = $(this).parent().closest('.sm-accordion-group').nextAll().find('.sm-accordion-heading');
    var prevall = $(this).parent().closest('.sm-accordion-group').prevAll().find('.sm-accordion-heading');

    $(this).parent().find('.sm-accordion-heading').next().slideToggle();
    $(nextall).next().slideUp();
    $(prevall).next().slideUp();

    $(this).parent().find('.sm-accordion-heading').toggleClass('active');
    $(nextall).removeClass('active');
    $(prevall).removeClass('active');
  });
}( jQuery ));
</code>
</pre>    
