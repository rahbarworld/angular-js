# angular-js
function HeroDetailController() {
  var ctrl = this;

  ctrl.delete = function() {
  http://www.routeforpurchase.com/deals
    ctrl.onDelete({hero: ctrl.hero});
  };
  ctrl.update = function(prop, value) {
    ctrl.onUpdate({hero: ctrl.hero, prop: prop, value: value});
  };
}

angular.module('heroApp').component('heroDetail', {
  templateUrl: 'heroDetail.html',
  controller: HeroDetailController,
  bindings: {
    hero: '<',
    onDelete: '&',
    onUpdate: '&'
  }
});

ar myMod = angular.module('myMod', ['ngRoute']);
myMod.component('home', {
  template: '<h1>Home</h1><p>Hello, {{ $ctrl.user.name }} !</p>',
  bindings: {
    user: '<'
  }
});
myMod.config(function($routeProvider) {
  $routeProvider.when('/', {
    template: '<home user="$resolve.user"></home>',
    resolve: {
      user: function($http) { return $http.get('...'); }
    }
  });
});
