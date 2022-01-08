# slides

//slider


    function showSlides(n) {
        if(n > slides.length) {   // если n больше количество всех слайдов то есть мы перелистали все фотки, то аргумент функции равно одному то есть первому,
            slideIndex = 1;
        }

        if(n < 1 ) {
            slideIndex = slides.length; // а если слайд меньше одного то он slideIndex равно общему количество слайдов т.е последнуму.
        }



    function plusSlides(n) {
        showSlides(slideIndex += n);
    }

    function currentSlide(n) {
        showSlides(slideIndex = n); // когда мы кликаем на четвертую точку на месте n пишется 4, и таким образом slideIndex принимает 4 ку и так выполняется 4 слайд
    }



    dotsWrap.addEventListener('click', function(event) {
        for (let i = 0; i < dots.length + 1; i++) { // здесь мы запускаем цикл на один раз больше
            if(event.target.classList.contains('dot') && event.target == dots[i - 1]) {
                currentSlide(i);
            }
        }  // если кликаем 4 точку, тогда индекс нашей точки будет 3( так как действие с нуля начинается) то сюда в квадратные скобки передается тройка dots[i - 1], 
        и здесь не стыковка потому что мы кликаем на 4 кнопку, а он у нас тройка, и таким образом при клике 4 точку в дот мы передаем 4 ую и таким образом в 
        в currentSlide тоже передается четвертая.
        

    
    
