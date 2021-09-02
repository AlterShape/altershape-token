
<!DOCTYPE html> <!--[if lt IE 7]> <html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]--> <!--[if IE 7]> <html class="no-js lt-ie9 lt-ie8"> <![endif]--> <!--[if IE 8]> <html class="no-js lt-ie9"> <![endif]--> <!--[if gt IE 8]> <!--> <html lang="en"> <!-- <![endif]--> <head></head> <body> <div class="menu_wrapper"> <nav> <input type="checkbox" id="show-search"> <input type="checkbox" id="show-menu"> <label for="show-menu" class="menu-icon"><i class="fal fa-bars"></i></label> <div class="menu_content"> <div class="logo"> <a href="/"><img src="https://altershape.com/default/template/img/logo.png?v=2" alt="Logo Alter Shape"></a> </div> <ul class="links"> <li> <a href="/" class="desktop-link">Home page</a> <input type="checkbox" id="show-home"> <label for="show-home">Home page</label> </li> <li> <a href="javascript:void(0)" data-id="about" class="desktop-link menu_go">Why use ASC</a> <input type="checkbox" id="show-discover"> <label for="show-discover" data-id="about" class="menu_go">Why use ASC</label> </li> <li> <a href="/default/template/login.html" class="desktop-link">Resources <i class="fal fa-chevron-down"></i></a> <input type="checkbox" id="show-pages"> <label for="show-pages">Resources <i class="fal fa-chevron-down"></i></label> <ul> <li><a href="/default/template/authors.html">Whitepaper</a></li> <li><a href="/default/template/single-author.html">Transparency</a></li>  <li> <a href="javascript:void(0)" class="soc_article" data-id="2">Usage rules </a> </li> <li> <a href="javascript:void(0)" class="soc_article" data-id="3">Privacy Policy </a> </li> <li> <a href="javascript:void(0)" class="soc_article" data-id="4">Frequently asked questions</a> </li> <li> <a href="javascript:void(0)" class="soc_article" data-id="5">Support</a> </li> </ul> </div> </div> <div class="col-lg-3 col-md-6 col-sm-12"> <div class="foo_widget footer_sub_form"> <p> Copyright © 2021 <a href="/">Alter Shape.</a> </p> </div> </footer><script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script src="/default/template/js/jquery.min.js"></script> <script src="/default/template/js/plugins.js"></script> <script src="/default/template/js/bootstrap.min.js"></script> <script src="/default/template/js/slick.min.js"></script> <script src="/default/template/js/jquery.stellar.min.js"></script> <script src="/default/template/js/owl-carousel.js"></script> <script src="/default/template/js/countdown.js?v=time();"></script> <script src="https://cdnjs.cloudflare.com/ajax/libs/magnific-popup.js/1.1.0/jquery.magnific-popup.min.js"></script> <script src="/default/template/js/main.js"></script> <script> $(".links .menu_go").click(function() { var href = $(this).data('id'); console.log(href); $('html , body').animate({ scrollTop: $("#"+href).offset().top }, 0); }); </script> <div class="modal fade" id="blog" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true"> <div class="modal-dialog modal-lg" role="document" style="z-index: 9999"> <div class="modal-content"> <div class="modal-body text-center"> </div> </div> </div> </div> <script> $('body').on('click', '.soc_article', function(){ var id = $(this).data('id'); $('#blog .modal-content').html('<div class="text-center p-5"><i class="fa fa-spinner fa-pulse fa-3x fa-fw"></i></div>'); $('#blog').modal('show'); $.post('https://altershape.com/', {'show_post':1, id:id}, function(data){ $('#blog .modal-content').html(data); }); }); </script> <script src="https://cdnjs.cloudflare.com/ajax/libs/toastr.js/2.1.4/toastr.min.js"></script> <script> toastr.options = { "closeButton": false, "debug": false, "newestOnTop": false, "progressBar": false, "positionClass": "toast-top-right", "preventDuplicates": false, "onclick": null, "showDuration": "300", "hideDuration": "1000", "timeOut": "5000", "extendedTimeOut": "1000", "showEasing": "swing", "hideEasing": "linear", "showMethod": "fadeIn", "hideMethod": "fadeOut" }; function submit_f(){ var email = $('input[name="Follow_Email"]').val(); function isValidEmailAddress(emailAddress) { var pattern = new RegExp(/^(("[\w-\s]+")|([\w-]+(?:\.[\w-]+)*)|("[\w-\s]+")([\w-]+(?:\.[\w-]+)*))(@((?:[\w-]+\.)*\w[\w-]{0,66})\.([a-z]{2,6}(?:\.[a-z]{2})?)$)|(@\[?((25[0-5]\.|2[0-4][0-9]\.|1[0-9]{2}\.|[0-9]{1,2}\.))((25[0-5]|2[0-4][0-9]|1[0-9]{2}|[0-9]{1,2})\.){2}(25[0-5]|2[0-4][0-9]|1[0-9]{2}|[0-9]{1,2})\]?$)/i); return pattern.test(emailAddress); }; if(email == ''){ Command: toastr["error"]("Trường không được để trống!"); $('textarea[name="Follow_Email"]').focus(); return false; }else if(!isValidEmailAddress(email)) { Command: toastr["error"]("Địa chỉ email không hợp lệ"); $('input[name="Follow_Email"]').focus(); return false; } if(true){ $('.submit_form').html('<i class="fa fa-spinner fa-pulse fa-fw"></i>'); $('.submit_form').attr('disabled', true); $.post('https://altershape.com/', {'submit_subscribe':1, Follow_Email:email}, function(data){ console.log(data); if(data.success == 1){ Command: toastr["success"](data.notifi); $('input[name="Follow_Email"]').val(''); }else{ Command: toastr["error"](data.notifi); } }); } } $('body').on('click', '.subscribe', function(){ submit_f(); }); $('input[name="Follow_Email"]').keyup(function(e){ if(e.keyCode == 13) { submit_f(); } }); </script> <script> $('#dropdownMenuButton1').click(function(){ if($('.dropdown-menu').hasClass('show')){ $('.dropdown-menu').removeClass('show'); }else{ $('.dropdown-menu').addClass('show'); } }) </script> <script> $(document).ready(function() { $('.client_carousel').magnificPopup({ delegate: 'a', type: 'image', tLoading: 'Loading image #%curr%...', mainClass: 'mfp-img-mobile', gallery: { enabled: true, navigateByImgClick: true, preload: [0,1] }, image: { tError: '<a href="/default/template/%url%">The image #%curr%</a> could not be loaded.', } }); }); </script> <script> var date = (new Date()).getTimezoneOffset(); function showTime(){ var date = new Date(); var h = date.getUTCHours(); var m = date.getUTCMinutes(); var s = date.getUTCSeconds(); if(h == 0){ h = 0; } h = (h < 10) ? "0" + h : h; m = (m < 10) ? "0" + m : m; s = (s < 10) ? "0" + s : s; var time = '<div>'+h+'<span>Hour</span></div> <div>'+m+'<span>Minute</span></div> <div>'+s+'<span>Second</span></div>'; $('#MyClockDisplay').html(time); setTimeout(showTime, 1000); } showTime(); </script> <div id="slide_1" class="modal fade" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true"> <div class="modal-dialog modal-lg"> <div class="modal-content"> <div class="modal-header"> <h4 class="modal-title text-dark">DeFi - decentralized finance</h4> <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button> </div> <div class="modal-body"> <div class="embed-responsive embed-responsive-16by9"> <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/yubzJw0uiE4?enablejsapi=1&version=3&playerapiid=ytplayer" allowfullscreen></iframe> </div> </div> </div> </div> </div> <div id="slide_2" class="modal fade" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true"> <div class="modal-dialog modal-lg"> <div class="modal-content"> <div class="modal-header"> <h4 class="modal-title text-dark">Developing useful technology products</h4> <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button> </div> <div class="modal-body"> <div class="embed-responsive embed-responsive-16by9"> <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/jZ4ZK7SkjCs?enablejsapi=1&version=3&playerapiid=ytplayer" allowfullscreen></iframe> </div> </div> </div> </div> </div> <div id="modal_about" class="modal fade" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true"> <div class="modal-dialog modal-lg"> <div class="modal-content"> <div class="modal-header"> <h4 class="modal-title text-dark">Introduce Alter Shape</h4> <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button> </div> <div class="modal-body"> <div class="embed-responsive embed-responsive-16by9"> <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/DnC4Q6T3BNk?enablejsapi=1&version=3&playerapiid=ytplayer" allowfullscreen></iframe> </div> </div> </div> </div> </div> <script src="/default/template/lib/youtube/main.js"></script> <script> $('.modal').on('hidden.bs.modal', function () { $('#slide_1 iframe')[0].contentWindow.postMessage('{"event":"command","func":"' + 'pauseVideo' + '","args":""}', '*'); $('#slide_2 iframe')[0].contentWindow.postMessage('{"event":"command","func":"' + 'pauseVideo' + '","args":""}', '*'); $('#modal_about iframe')[0].contentWindow.postMessage('{"event":"command","func":"' + 'pauseVideo' + '","args":""}', '*'); }); </script> </body> </html>
