# pong
Very simple socket server

## Compiling

Nothing special is needed to compile the binary:

    cc -o pong pong.c

You can also use make to compile:

    make

## Demo

A demo can (some times) be found at http://cyclonecode.tk:8000/

### Adding quotes for the demo

You can add your own quote which will be displayed at the end of the response at https://cyclonecode.tk:8000/ by going to
https://cyclonecode.tk/quote.php and add something interesting =)

## Running

Depending on which port you are using you might need to run the program with sudo privileges.

    sudo ./pong 3000

You should then be able to connect and get a quote:

    curl 127.0.0.1:3000

You could also go to http://127.0.0.1:3000 directly in your browser.

Notice that the program assumes that there is a `banner` and `quotes.txt` file, the contents of these files is not really important; each line in `quotes.txt` becomes a random response from the server, while the contents of the `banner` is sent as it is.

You may also use the `-b` switch to specify a different banner file:

## Syntax

    b <banner>  Specify a custom banner file.
    q <banner>  Specify a custom quotes file.
    x           Do not send any banner.
    w <ip,...>  List of whitelisted ip addresses to allow.
    v           Verbose logging. Entire request will be logged.
    s <name>    Set name of server. Sent in 'Server' header in response.

## Example output

<pre style="font-family:monospace;">
$> curl 127.0.0.1:3000
                                                        ..,***//((#%@@@@@@@@@@@@@@@%##(//***,...
                                                      .,*//(%%%%  @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@   %%%((/*,..
                                              .,**(#%% @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@  %#(**,.
                                           ..,/#%% @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ %%#/,..
                                      ..,(%  @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@  %(,..
                                     ,//# @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@//,
                                 ,,/% @@@@@@@@@@@@@@@@@@@@@@@@   %%##(//****,,,,.......,,,,****//((#%%   @@@@@@@@@@@@@@@@@@@@@@@@ %/,,
                              ./%@@@@@@@@@@@@@@@@@@@@@  %((/*,..                                        .,*//(%   @@@@@@@@@@@@@@@@@@@@%/.
                            ,,(%@@@@@@@@@@@@@@@@@@@ %%(/*..                                                  .*/((% @@@@@@@@@@@@@@@@@@@%(,,
                          *#  @@@@@@@@@@@@@@@@//,.                                                               .,//# @@@@@@@@@@@@@@@@ *
                         *# @@@@@@@@@@@@@@@ /,..                                                                   ..,/#  @@@@@@@@@@@@@@@*
                      ,## @@@@@@@@@@@@@@*..                                                                             ..*# @@@@@@@@@@@@@@#,
                    ./%@@@@@@@@@@@@@@%//.                                                                                     .//%@@@@@@@@@@@@@@%/.
                  ..*%@@@@@@@@@@@@@ %*..                                                                                       ..*% @@@@@@@@@@@@@%*..
                 .(( @@@@@@@@@@@#,                                                                                               ,## @@@@@@@@@@@ ((.
                 *%%@@@@@@@@@@@@%**                                                                                                 **%@@@@@@@@@@@@%%*
               ./ @@@@@@@@@@@@%/.                                                                                                     ./%@@@@@@@@@@@@ /.
              ./ @@@@@@@@@@@##,                                                                                                         ,##@@@@@@@@@@@ /..
              ,# @@@@@@@@@@%**                                                                                                           **%@@@@@@@@@@,,
            ..( @@@@@@@@@@%*                                                                                                               *%@@@@@@@@@@ ((.
            **%@@@@@@@@@@ (.                                                                                                               .( @@@@@@@@@@%%*
           .(( @@@@@@@@  (.                                                                                                                 .(  @@@@@@@@  (.
           *%%@@@@@@@@@##,                                                                                                                   ,##@@@@@@@@@@%*
          ./  @@@@@@@@ ((.                                                                                                                   .(( @@@@@@@@@ /.
          ,%@@@@@@@@@@%,,                                                                                                                     ,,%@@@@@@@@@@%,
          *%@@@@@@@@@ (..                                                                                                                     ..( @@@@@@@@@%*
        ../ @@@@@@@@@%/                                                                                                                         /%@@@@@@@@@ /..
        ..( @@@@@@@@@%*                                                                                                                         *%@@@@@@@@@ (..
        ..#@@@@@@@@@@%,                                                                                                                         ,%@@@@@@@@@@#..
        ,,%@@@@@@@@@@#.                                                                                                                         .#@@@@@@@@@@%,,
        **%@@@@@@@@@@#.                                                                                                                         .#@@@@@@@@@@%**
        **%@@@@@@@@@@#.                                                                                                                         .#@@@@@@@@@@%**
        ,,%@@@@@@@@@@#.                                                                                                                         .#@@@@@@@@@@%,,
        ,,#@@@@@@@@@@#.                                                                                                                         .#@@@@@@@@@@#,,
        ..#@@@@@@@@@@%,                                                                                                                         ,%@@@@@@@@@@#..
        ..( @@@@@@@@@%*                                                                                                                         *%@@@@@@@@@ (..
        ../ @@@@@@@@@%/                                 .........                                       ......                                  /%@@@@@@@@@ /..
          *%@@@@@@@@@ (..                         .,((#%   @@@   %#((,.                         .**(#%        %%((*,                          ..( @@@@@@@@@%*
          ,%@@@@@@@@@@#,,                       ../#  @@@@@@@@@@@@@ /.                       ,(%% @@@@@@@@@@@@  %(*..                       ,,#@@@@@@@@@@%,
          .(  @@@@@@@@ //......               ./%%@@@@@@@@@@@@@@@@@@@@@%//.                 ,,( @@@@@@@@@@@@@@@@@@@@@%%/.               ......// @@@@@@@@@ (.
           /  @@@@@@@@#((#((/,.            ./%@@@@@@@@@@@@@@@@@@@@@@@@%%*                .//%@@@@@@@@@@@@@@@@@@@@@@@@%*             .,/((#((## @@@@@@@@@ /
           ,##@@@@@@@@@@@@@@@@@@#,,        ../ @@@@@@@@@@@@@@@@@@@@@@@@@@@%*              ./  @@@@@@@@@@@@@@@@@@@@@@@@@@ /..        ,,#@@@@@@@@@@@@@@@@@@@#,
            // @@@@@@@@@@@@@@@@@ //.       **%@@@@@@@@@@@@@@@@@@@@@@@@@@@@@%,             *%@@@@@@@@@@@@@@@@@@@@@@@@@@@@@%**       .// @@@@@@@@@@@@@@@@@  /
            ,,%@@@@@@@@@@@@@@@@@ //.      .(( @@@@@@@@@@@@@@@@@@@@@@@@@@@@@%*             *%@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ ((.      .// @@@@@@@@@@@@@@@@@%%,
              *%@@@@@@@@@@@@@@@@%**       *%%@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ /..          ./ @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@%%*       **%@@@@@@@@@@@@@@@@%**
              ,#@@@@@@@@@@@@@@@@%,,       /  @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ /..          ./ @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@  /       ,,#@@@@@@@@@@@@@@@@#,,
               *%@@@@@@@@@@@@@@ /..      .(  @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ /..          ./ @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@#.        / @@@@@@@@@@@@@@%*
               .( @@@@@@@@@@@@@%*        ,#@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ /             / @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@%,        *%@@@@@@@@@@@@@ (.
                .(  @@@@@@@@@@@%,        ,%@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@#,             ,#@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@%*        .( @@@@@@@@@@  (.
                 .(( @@@@@@@@@ /.        .#@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@%*               *%%@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@%,         / @@@@@@@@@ ((.
                 .// @@@@@@@@@ /         .(  @@@@@@@@@@@@@@@@@@@@@@@@@@@  (.               .(( @@@@@@@@@@@@@@@@@@@@@@@@@@@@@#,         *%@@@@@@@@@ //.
                 .// @@@@@@@@@%*          ,%%@@@@@@@@@@@@@@@@@@@@@@@@@@%//.                 ../%@@@@@@@@@@@@@@@@@@@@@@@@@@%%*          *%@@@@@@@@@ ((.
                 .// @@@@@@@@@%*          .(( @@@@@@@@@@@@@@@@@@@@@@@@%(..                    .(%@@@@@@@@@@@@@@@@@@@@@@@@#,          *%@@@@@@@@@ ((.
                 .// @@@@@@@@@ /.          ..*%@@@@@@@@@@@@@@@@@@@ %%/,          .,,,.          ,//% @@@@@@@@@@@@@@@@@@@%/..           / @@@@@@@@@ //.
                  **%@@@@@@@@@@%*              ,//(%%%%     %%%%(*,            ,(%@@@%/..           ,*((%%%     %%%%(//,.             *%@@@@@@@@@@%**
                  ,,#@@@@@@@@@@,,               .,***//////*,,.            ..(%@@@@@%//.            ..,*//////***,.               ,,# @@@@@@@@@@%,,
                    *%@@@@@@@@@@@  (*.                                     ./%%@@@@@@@@@@%*                                      .*(  @@@@@@@@@@@%*
                    ,# @@@@@@@@@@@@ %(**.                                  ,#@@@@@@@@@@@@ (,                                  .**(% @@@@@@@@@@@@,
                     .(  @@@@@@@@@@@@@@@ %(**.                            *%@@@@@@@@@@@@@@@%**                           .**(% @@@@@@@@@@@@@@@  (.
                      .**%@@@@@@@@@@@@@@@@@@@*..                      **%@@@@@@@@@@@@@@@@@%%*                      ..*# @@@@@@@@@@@@@@@@@@@%**.
                       ../%@@@@@@@@@@@@@@@@@@@@%**.                    .(( @@@@@@@@@@@@@@@@@  (.                    .**%@@@@@@@@@@@@@@@@@@@@%/..
                          .*((% @@@@@@@@@@@@@@@@  (.                  .(  @@@@@@@@@@@@@@@@@@@@ /.                  .(  @@@@@@@@@@@@@@@@ %((*.
                            ..*#%  @@@@@@@@@@@@@@@%*                  ,#@@@@@@@@@@@@@@@@@@@@@@@#,                  *%@@@@@@@@@@@@@@@  %#*..
                                 ,,*(%@@@@@@@@@@@@@#,,               ./ @@@@@@@@@## @@@@@@@@@ /..               ,#@@@@@@@@@@@@@%(*,,
                                      **#@@@@@@@@@@%**               .(@@@@@@@@@@%**,( @@@@@@@@@(..               *%@@@@@@@@@@#**
                                      ../ @@@@@@@@@%**               .( @@@@@@@@ (.. *%@@@@@@@@ (..               *%@@@@@@@@@ /..
                                        *%@@@@@@@@@ //.               ,#  @@@  %*.    ,(( @@@@,               ../ @@@@@@@@@%*
                                        *%@@@@@@@@@#,               .*((%%%##*.      ,,(%%%%(*.               ,,# @@@@@@@@@%*
                                        ,#@@@@@@@@@@@@#,                                                       ,##@@@@@@@@@@@#,
                                         *%@@@@@@@@@@@@%(,,                                                  ,(%@@@@@@@@@@@@%*
                                         .(  @@@@@@@@@@@#*.                                             .**# @@@@@@@@@@@  (.
                                          .(( @@@@@@@@@@@@@@%#//,.                                   .,,/#%@@@@@@@@@@@@@@ ((.
                                           ,,#@@@@@@@@@@@@@@@ %%#/*..                              .*/##% @@@@@@@@@@@@@@@#,,
                                             .*%@@@@@@@@@@@@@@@@@@@   %#((/****,,.....,,,***//(#%   @@@@@@@@@@@@@@@@@@@%*.
                                               .**# @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@**.
                                                ..*(%%@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@%(*..
                                                    ..,(%  @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ %(,,.
                                                       .*((% @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@ %%(*.
                                                            .,**(#%   @@@@@@@@@@@@@@@@@@@@@@@@@@@   %#((*,.`

I have a question for you: Who is Ice-T?
</pre>
