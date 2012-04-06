# jQuery smash event #
A keyboard smash event for jQuery allows you to detech when the keyboard was smashed.

## Example ##
    <input id="smash" type="text" value="" autocomplete="off" />

    <script src="/js/jquery.smash.js"></script>

    <script type="text/javascript">
    $(document).ready(function() {
      var smashed = function(e) {
        var $smash = $(this);
        $smash.blur().attr('disabled', 'disabled');
      };
      $('#smash').on('smash', {
        keypress_time_diff: 200, // time to allow between keypresses
        smash_time: 1000 // total time to listen for smash
        }, smashed).focus();
    });
    </script>
