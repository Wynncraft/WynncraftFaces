$(document).ready(function() {
    // Json Fetch
    $.getJSON(
        'http://api.wynncraft.com/public_api.php?action=onlinePlayers',
        function(data) {
            $.each(data, function(key, obj) {
                var server = key;
                $.each(obj, function(key, obj) {
                    var player = obj;
                    // Check if player defined
                    if (player.length !== 0 &&
                        server !== "request") {
                        $('<img/>', {
                            id: player,
                            src: 'http://api.wynncraft.com/avatar/' +
                                player +
                                '/64.png',
                            "data-toggle": 'tooltip',
                            "data-original-title": player +
                                ' online on server ' +
                                server,
                            "data-placement": "top"
                        }).appendTo('#online');
                    }
                });
            });
            // Set tooltips
            $('[data-toggle=tooltip]').tooltip();
        });
});
