jQuery(function ($) {
  "use strict";

  // Remove Navbar Fixed Class On Scroll
  var navFixed = $(".navbar-fixed-top");
  $(window).on("scroll", function () {
    $(this).scrollTop() > 200 ? navFixed.addClass("home-nav") : navFixed.removeClass("home-nav");
  });
  $(this).scrollTop() > 200 ? navFixed.addClass("home-nav") : navFixed.removeClass("home-nav");

  // Learning Paths Show Content
  $(".step-title").on("click", function () {
    $(this).toggleClass("opened");
    $(this).next(".step").slideToggle();
  });

  // Scroll To Top
  var scrollToTop = $(".scroll-to-top");
  $(window).on("scroll", function () {
    if ($(window).scrollTop() >= 500) {
      if (!scrollToTop.is(":visible")) {
        scrollToTop.fadeIn(300);
      }
    } else {
      if (scrollToTop.is(":visible")) {
        scrollToTop.fadeOut(300);
      }
    }
  });
  $(".scroll-to-top span").on("click", function () {
    $("html, body").animate(
      {
        scrollTop: 0,
      },
      1000
    );
  });

  $(window).on("load", function () {
    "use strict";
    $(".tutorial-demo style").detach().appendTo("head");
  });

  // Goals

  $(".goal-box").each(function () {
    var has = $(this).find(".has").data("has");
    var target = $(this).find(".target").data("target");
    var percentage = (parseInt(has) * 100) / parseInt(target);
    $(this)
      .find(".the-background span")
      .css("width", percentage.toFixed(1) + "%");
    $(this)
      .find(".the-handle")
      .text(percentage.toFixed(1) + "%")
      .css("left", percentage.toFixed(1) + "%");
  });

  // Total Goals
  var totalHas = 0;
  var totalTarget = 0;

  $(".goals-container .has").each(function () {
    totalHas += parseInt($(this).data("has"));
  });
  $(".goals-container .target").each(function () {
    totalTarget += parseInt($(this).data("target"));
  });

  var totalPercentage = (totalHas * 100) / totalTarget;

  $(".all-targets").each(function () {
    $(this).find(".all-has").text(totalHas);
    $(this).find(".all-target").text(totalTarget);
    $(this)
      .find(".the-background span")
      .css("width", totalPercentage.toFixed(1) + "%");
    $(this)
      .find(".the-handle")
      .text(totalPercentage.toFixed(1) + "%")
      .css("left", totalPercentage.toFixed(1) + "%");
  });

  /*
   ** Task Rating
   */

  $(".challenges-rating li").on("click", function () {
    $(this).addClass("active").siblings().removeClass("active");
    $(".challenges-child > div").hide();
    $(".challenges-child " + $(this).data("class")).fadeIn(300);
  });

  // Study Plan
  $(".the-study .toggler").on("click", function () {
    $(this).toggleClass("open");
    $(this).next(".all-steps").slideToggle(200);
  });
  $(".the-study .side li").on("click", function () {
    $(this).addClass("active").siblings().removeClass("active");
    $("html, body").animate(
      {
        scrollTop: $("[data-week=" + $(this).attr("id") + "]").offset().top + 3,
      },
      800
    );
  });
  $(window).on("scroll", function () {
    if ($(".the-study").length) {
      if ($(window).scrollTop() >= $(".the-study").offset().top) {
        $(".the-study").addClass("passed");
      } else {
        $(".the-study").removeClass("passed");
      }
      $(".week").each(function () {
        if ($(window).scrollTop() >= $(this).offset().top) {
          $(".the-study .side li").removeClass("active");
          $("#" + $(this).data("week")).addClass("active");
        }
      });
    }
  });
  if ($(".the-study").length) {
    if ($(window).scrollTop() >= $(".the-study").offset().top) {
      $(".the-study").addClass("passed");
    } else {
      $(".the-study").removeClass("passed");
    }
  }

  // Sort Supporters Table
  var sorted = $('.youtube-supporters table tbody tr').sort(function (a, b) {
    var a = $(a).find('td:last').text(), b = $(b).find('td:last').text();
    return b.localeCompare(a, false, { numeric: true });
  })
  $('.youtube-supporters table tbody').html(sorted);

});
