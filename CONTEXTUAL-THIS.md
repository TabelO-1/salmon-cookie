
  calcCustomersEachHour: function () {
    for (var i = 0; i < hours.length; i++) {
      this.customersEachHour.push(random(this.minCustomersPerHour, this.maxCustomersPerHour));
    }
  }
This in calcCustomersEachHour takes whatever is being inputed, for example seattle, and takes it's customers each hour and pushes seattle.minCustomersPerHour, and seatle.maxCustomersPerHour and does it for all the hours in the hours array.


  calcCookiesEachHour: function () {
    this.calcCustomersEachHour();
    for (var i = 0; i < hours.length; i++) {
      var oneHour = Math.ceil(this.customersEachHour[i] * this.avgCookiesPerSale);
      this.cookiesEachHour.push(oneHour);
      this.totalDailyCookies += oneHour;
    }
  }
This is still the same in calcCookiesEachHour, however it's being used differently, this is taking seattle.customersEaachHour[i] and multiplying it by seattle.avgCookiesPerSale. Then is takes seatle.cookiesEach hour and pushes it by the var (oneHour). Then it takes this.totalDailyCookies(which was caculated) and adds it to oneHour.
This is used to take input from an object and be used in a function.