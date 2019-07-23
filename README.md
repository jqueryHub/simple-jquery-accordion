Simple Jquery Accordion
=================================

Simple Jquery Accordion is very simple

[Article on jqueryHub](#)

[Demo](#)


How to use
==========

=> Add basic HTML structure of accordion.

        <div class="sm-accordion">
          <div class="sm-accordion-group">
            <div class="sm-accordion-heading">Accordion Heading - 1</div>
            <div class="sm-accordion-content"> ..... </div>
          </div>
          <div class="sm-accordion-group">
            <div class="sm-accordion-heading">Accordion Heading - 2</div>
            <div class="sm-accordion-content"> ..... </div>
          </div>
          <div class="sm-accordion-group">
            <div class="sm-accordion-heading">Accordion Heading - 3</div>
            <div class="sm-accordion-content"> ..... </div>
          </div>
        </div>


=> Add accordion script.

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
