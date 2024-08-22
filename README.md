<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Магазин</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            text-align: center;
        }
        h1 {
            color: #333;
        }
        .product-image {
            max-width: 100%;
            border-radius: 10px;
        }
        .price {
            font-size: 24px;
            color: #e67e22;
            margin: 15px 0;
        }
        .buy-button {
            background-color: #2ecc71;
            color: white;
            border: none;
            padding: 15px 25px;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
            text-decoration: none;
        }
        .buy-button:hover {
            background-color: #27ae60;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Название товара</h1>
    <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxISEBUQEhIVFRUVFRUXFxUVFRUYFRUXGBUWFxUWFRcYHSggGBomHRUVIjEhJSkrLi4uFx8zODMtNygtLisBCgoKDg0OGhAQFy0lHx0tLS0tKy0tLS0tLS0tLS0tKy0tKystLS0tLSstLS0tKystLSstLS0tLS0tLS03Ky0tLf/AABEIAO8A0wMBIgACEQEDEQH/xAAcAAABBQEBAQAAAAAAAAAAAAACAQMEBQYABwj/xABBEAABAwIEAwYDBQUHBAMAAAABAAIRAwQFEiExBkFREyJhcYGRBzKhQrHB0fAUI1JicjOCkqKy4fEVJMLSQ3Oz/8QAGAEAAwEBAAAAAAAAAAAAAAAAAAECAwT/xAAgEQEBAAIDAQADAQEAAAAAAAAAAQIRAyExEiIyQVFx/9oADAMBAAIRAxEAPwC2aE4AhATgCaCgJVyMBBOaEYC4BEAgOARwuASpB0JVwCIBMEAWcxPjmxoHKa3aOHKkC/XpmHd+qxXxH4ydUe+zoOLaTSW1HAkGo4aOb/QNR4x0WAaUlSPXD8UbadLeuR1/dj6ZldYTxtZVzlDzTcdhVGUHyd8s+Erw+m5Sqf66IPT6KAXZV5l8PuJXU3ttqriaT+6wn/43ch/Sdo5GF6hlQmw0QuhOQuhMjcLoTkLoQDRCSE6QhIQDWVCQnSEJQDJCAhPOCAhANQuTmVcgIwCcAQtRhAKAjASNCcAQHAIwFwCWEAqWFwCMBAIAqjjHEzbWNas35g3K09HPOVp9CZ9FdBYz4tk/9PaB9q4pg+WV5H1ASOPGBTJ2lOUrV52BWxwXCmCh3xJzTymITZy03HKNJ/RU7bTFm6djUzZQDtyGv+6kGxc3kdg478zAC9LwJ7GBteB32mBH2hp962mBsolhLmMe4gSS0axsB0hEouOngTAQPBe58LXpr2dGq4y4shx6uaS0k+cT6rH/ABAsabnDsmAFk5i0a69Y8gtH8O2Rh1P+qp/+jh+CcqM5poCEkI4XQqQCF0I4XQgjZCQhOQkIQZohCQnSEJCCNOCbITxCAhANwuRwuQaIAiaEgTjQghAIwkaEYCQcAiAXAIwEw4BGAkCIBIOAXnnxSpPfVoMzwwgZWS7v1M+sAd0w0bnaRG5XosLLfEGzzUqFWJNKsD5BwM/dHqlV4+snc2xo0niTmawGIJAB6wOWknlKz+F12VazGkhuZ4BnYAmJ1W94mFPK6sWj5SMjs2So17diGkSRMiNiBvqF5WLMl7QwO0+Ykkk66kQBClq9BxWoyjTp06feADyHAyPn7x8umvMKy4Y4vtqZyVTBiGhoJJPkFn8IwV1enV7Nz4a1rKYPyy8S7MI1aCN9DtsqrhjCqtK+Y2sH0SHnP3JLh1pu/ESPPZKLur09Lwqmyq+oYPfLtHfMAdBI67Kw4RollnTpn7II+Ut13doTrqTrzUDDsOqCqx5cXOZnO0S0EuE8zvGqv8KshRo06Qk5GgSdyeZPrKrFnypBCGE4QkhWxBCWEQC6EAEJCEcJCEgaIQkJ0hAQmDTghITpCAhBG1yKFyAhtCcaEDQnWhICARtCEI2hAKAjASBG0IBQES4JQEG4BQ8bo5raqInuOI8wJH3KcAlcyQQdiCD5FAjA4pR7a07I6FveYfIHQ+6wmHmoHPe1shoyu9dNOsaLW4jeOYalDZ7SWfWJ8uar20e2pMt7Yjtu8cjXQ9zRIJ/Hfms3RKvOArlrGVW1KwYSeZIdmM7e0qTw3xO4uqtqjNUpOLDAI1BIDwDqARrr1UDAuHbiye64q0X9k0CXHsyWkbmTU2MxuoV3dsfeftFMgio2HAdIDqZj/F7hK+Lnr0HAqxc4uPMFW0LPcIElrjy/30/FaOFeHjDk/YMJIRwuhUzBC6EcJITAYSEIikSBshCQnSEBCYNEISE6QgIQAQuRQuQSA0J0BA0I2oAgnGhC1OBAKEaQBEEjKEbQhCxHEvH7aZNO1Ae4aGq75B/QPtee3mlaeONrX4nidG3Z2lZ4YOXVx6NaNSfJYTEuNK9w7s7YGkz+PeqfXZnpJ8VjLi/fXf2lZ7nvPNx+gGwHgNFeYM5tJwnn+gouTfHiiNilo6mzNJJdEkmTM6meuv0VnhGHWtSTUaHNq0+yOUtbVpOaRFSm52gcBOh3nwRcSvy25dpyWM/bJ2LmnnBI1/JBzUr1K24Yt2NJrXdzeSHNp0rl4fRpkgjtXNkgkASI/wCMfWsg27yUR3A0BonaO6ASq7DsUyiHVHu8C45R4xzWg4bql9X+zIB2J6o/6fX8a3DqbqTWtpPOaJeNxm8Rsrqji0aVm5D/ABCSz15t/Wqi2VHJ3oVld3dAMzPc3yJE+yUuhcZf4lMcCJBBB2IMg+RSwsW7iC3pvPYvIM/K0S0/1Db8Ve4dxJRqiHHI7x+X0PL1VzOVllxZRbpCEtN4cJaQR1Bke4SwqZgKEpwhCUACQhEUhQDbghIThQFMAhIjXICvajAQtTgQkTQjASBE1AGAqTiTimjZ91wL6hEim0xA5Fzvsj3Pgp2L33YUXVNyNGjq47fn5AryS/ove8veS5zjJJ3JKjLLTbj4/rtN4g42uLlhpgClTO7WEku8HOMSPAALIVHGVeUrQE6pm/swNlH03+NKqjJOhKfFSoDo5SbezU6nY+CX0cwqLVu6tRgpvMgK/wAC4bZkm5aQyq05Hc2lvPwSWdhrstxZYY025DgSAOp6bpbtO4yevLG2AY90mWh2k8+i9EwGvRZSa9gzuI9J6Lz69ol1Z0bBxiVreHmljYJhG1fLR031am78oPJvIeqOth0Az3tCNd0AqEKbSvTsUrqibnjzelhj6dZ0gxmJC1mGYQ52u2iu7izFQZmgSNUGD3ozFpEFu4O/P8kvj/TvJqdBsbV1KpBOV3Jw2Pg4cwtFb1MzQeexHQ80l7RFVmYbhRcFq5nlnNwOn8zfzH3LXH8bpz5z7m/6noSiSLVzgIQlOFAUgEoHBOFCUEbXJVyYQGpxqAIwgjiJoQhG0ICqxil2j20+TW5j/eJA/wBJ91n8YwhrGZiFpi4ftDweTGe0u/3Wb48xQDuN6LHJ1cdskjD3VxlJA6pyvavGrgfVUVzdw6eY1XqtjiNpdsDXQ1zgPuRMVXPth7caq5tmTyS8QYH2Ds7NW9Rt5KHh98P0VFjXHKVpsLs8zwNgthToZaRaOh+5ZbB7iSFsq1QZQfoqx8RyXt4ddVIuXgHTMfvWjsLnTZZHiOgaV9VY0yM589TKvMOrGNVOUaYZNTTuSVOtnEnZUlrUnRbLh6zDiEsZujOyQ5Z0HbwVXcY2/ZsFwzR7fm8QtleOZSpkleV8a8RTTe3ly8yQFpdTphN5Xf8AjQcLcSio0AnzUt1x2NznGwc148p1+i8XwbGnsq56ZiTq07HzC9Utq4rUhVkyW6zyPMKM9tcNVuLpoD3AbTp5HUJopu0rl9NjzuWNn/CE4V0RxWaoShKIoXIIJQlEUJQArly5MIARtTbU41CTgTgTYQ3dwKdN1R2zQT59B5kwPVI4pr24H7W9rdxSaD/VLnR7OC874tuCXkndbDDsWp0356kFziS7zJk+klZni57KrnPYNCsq68Zqaef1XmSt1wlw+bmnnD8sQB6ASVhbxkEhar4ecQGgch2BmPAqr4ievUr3CgLI0ycxaN15fTflfB6/mt1jPEYNMkHulpnrtsvN7i5zuzjSUrNnhdetvhdQSIP1W3rXWWiD8zjoB4+i8bsL4tcDr7r0/AcQbVot6t3lTOml77eRY/WP7dVc/ftDKtrO8boEPGuHntnVGiZJVZa1YIR7BLqtZQuoPVavBeIxTb5Lz+3uwCTGpCIYjBA6+3qlJYu3GztusZ4jdVETAXmfF2Iicg3P5a/erntSdZWHvmPe51bKcmfIHcs0TlnrGqMMd5bqeTKTH5jY8EYdTrNl3zBel4Kymab6LQMwErx3g7EjRrAcivWLAxWp1meEjqDuPZF9E/VtKFu1tvSc3bKAfAgfr2QlJReGvNP7D+83wO5H4p65oljsp8x5FbTxyZTswUJRSgKaSFC5EUBQArly5MkBqNqAFG1IjgVHxjWPZNpDd7pPk2PxLfZXjVRY0M9zTp/yA+7nf+oSq8PWRv8ABXigKh3Lo8YVBUMDeVt+PMUbRpMoN/tHAmB9lu2Y/WPJYWg6Qsr068btnsZHf05gKHa1ixwcNCFocMwo3d7TocnOAcejRq4+jQT6LX/F/hdrGi+osAHdZVA0jZtN/wBzT/d8VpPGGV/Jnbe5NRg0kdOSjXNB0/KR6K2+HTw7NTcJhpcB1jkFsrHGbeqHNNMFo7pMd5p5T4JK28xp03TABWmwK5qNGXMRO8JjiFjaNZzWDTceRVXQunAyFFa49NxcMYW97WU5ZcC07hpeyplPIESPWFla2LkgAq94X4q7F4BOh9kseqrPudDueBLlmmVpHVjgR7GCqevhD6Rh+noV6lecRMNPMOYWCvLs1+0eT3WR6k7AJ5XXiePG31SXrw2m4N3grW23BB/6C62Lf37/APuR1FXdrfPIMnqVQcMUm1L6i1wlrnkEdRkdovYyVXH4z57qyPlykYIcFu+HsYPd722hUb4m8P8A7NeF7BFO5l7ejag/tG+5B/veCzeGXEOARlFcWT3ChiOekGH5m6sP1jzCvLDE/wBooU3HduZp9CvO+H8QDm5SdRstLwzULHvYQQ2oZaeQcJkHzEx/Slhexy4zTRlCVxKRauUiByIlAUw5chXIJBajCbanAkRxqz1/dU23hc94bla1gkgSYLj/AKld3FcMYXnlt4k6Ae5C88xvJWrtpkk/MXHaXH9H2CWVaceO6zvEWIGtc1Kp+07ujowaMHsPclIwxSnqqjGqL6FXs3SR9l3UfmFPBLwxg3MaDfpp4qLHRjlptPhLh01at0R8oyN83an1AH+Zaj4lUw7CrkHk1p9qjD+Cm8M4ULW2ZR+18z/6zv5xAHoq/wCJNy1mF3Gb7Yaxo6uc8R9AT6K5OnNbu7ec8E2Wan2rXFr2OHeHKdp8CtzgmH03dpWA7J4JFQtcYfzmOiyfAgLKbj9l4iPFaeuXtY7ID3twPJS2ZLH741q5c4zBgachsm7S3Dt1X4mSKhlHY3ZCmtcbEnELPLsncKoNzjMOaC5vM2iZs65zwNdVKunptxhFJ1CWuI06+Cxxw7PWZbsMB5Mk+Akn2BVuMTc2iQeipLGrVdWFRjddhptOn4oyGHUq24UtAMQYG/LTzfcR+K9NKxPCtqaNzlqfM4b+JW0K04505+e7yUfGmAi9tXUhAqNOek48njlPIESPWeS8GuKLqb+8CCCQ4HQtcDDmkcjIX0nK8t+L+Chgbe0xGdwZVA2Lolj/ADhpB8mqrGeOWmfwq5LKL7jNApAE+M6ADxkj3V1wTxLUfVyPdo4BwH8LtC0nx2WRsLhptK1IjV0aydI10GyLhWp++DufT2Wfjp/ayPoPQtbUHyuHseY90BTHDT+0oupcxD2+cQ4fcnSVrLuObKauiFCUpKAlNDlySVyAgtRtTbU41BKbii5hjKY3Li4+DWg7+ZP0KwFpWmuXE7lavGrtva1HOPMsb5N0++Vn+HaP/cFw5Tqss66+GaifjGFtrtykA89ZBGnLTdVfC1oBidFmSWhxI3J7rS4OM+LQVpqLw5zz0BPsJlHwNbj9oq1IktY0A9MxM++VLG96VyzWNrbrzb4z3Ry2tDk51SofNoa1v+ty9IBXnXxmsSaNC4A0pvcx3gKgBBPqyPVa1yY+qnBbhrKLW+M/ctUcRpCkZPJeV2uIQAFYjEZbBKhuTErgGq4+KGkAdlEqOBKtsBo56jWSBJ3dsElbVlxUg5eaueGKQdUGYAhQeJbGtTuC1xY9m7XNaNPCYBVtwg5ufURHsgStxUtqQZsE1hzBnEDZM3VedAnrGuG6pX1U8ScYlrhUG4IWms7jtGB55rEYnekjx6LZYbRLKLGHcNE+Z1P3qsPWfL+sSiVVcT4U26tKtBw3bLY3D295hHqB7lWa5aOd80UtNOoH1U7DmZXA9Cr3jvBjRv6kNhj/AN4yNod8wHk7Np5KqpMWVdOFev8AB2IDKx5MFoIPjK01+3vkxo4Bw9d/rK8bwXFSzuTAXpeF4watGm17HBzZbnjuubyO8g+iMMv4ObDf5RPKBxRFAVq5iLki5BILU6xMsWQ4s4lLKn7O0mm0fO4yHO/pAIIb46T5bq3Sscd1W8Q031HvIHdbVcNeZJJ08vxQYRIkAGRvoYE9TyUKnxSKTiyk9wY46ggZfVpnTrELU8INZVq3doaw7R+Un+CAe66n4agR5LG9uvHURqlaGEczH6+i0HBlqW0nvIjO4R5NB193H2UKywdznlrtMphx6RyHitVSYGtDWiABACrDH+s+bklnzDwKy/xPugzDKsgHOabAD1LwfeGlaaVW8S8Pi/talAuy/K5ronK4HTTmNx6rVzx8+NeOSep1VbYxwRe2xM0TUYPt0u+I8QO8PUKiYVLaVMFRTLS5IO6rGlPUnJaOVdVLwv3M+an4XUynRUNNyuMPqBLSpWko1yVNFaAq2212V3h2GuqmGtc7waCT7BLSvpV0ap7dhOsOBA8eS9MBUPhjgUsrC4uIGUyykIJnkXkaegn8Fa4rRy1CQIaTp7a/WVeMYcl3UaUkoJXSqZoGOYRTuqeR+hGrHjdh6jqOo5rzjE+HKlB2Vw32cPld5fkvVUFWk14LXAEHcFKzasc7HlmB4MarqncJNNjjHJxLTl19CfRXHBHENUObaVKjMoc4doeQAJ7MHdx0Op221UjiKg+0a4MqZKVUFvaS0Gm4gw1znDY66rHYTb2ABFQ3LHtcctSlUBBHJwa4ETusrHTMtx7Ca9MOyioOve09pKUkciD4gysPh1pQuv3bbl9X+HtGtbUafFwIzey0WA4SbVj6ZeXHOTJ5CAA0eG/urxrHkxmtrOVyGVytihMK8p4w4eNC5fWqVcwqlz2k76uMA9YAXqgWJ+IHDTqs3bHuJaIcx0uytHOn0HMjxnqlV4XtgajqP8z3f4WjyA1+q0fDVxTL6X7t7KjagINKcxYdxA6rKNYRrP4Kxs3lsO7UNgyMmrp6ys7HRjXvFN4IDgZBEz1nmiBVJwnXc+1a52bwzbkQJPlOaFcrSObKaukm0p53hvU/Tmr3sIblA0EaKv4fAl7iYytGp5AyT9ysLRz3h1R3da8jK2NQ3q49ToY5ecqkoRto3b+agYnw5aXE9rRpvPV7Bm9HjvDzlaK3qS0k8y6PRxj7gnQGl0Eb6fSSfZPQeZXfwksn/wBmatP/AOuqHD2qgn6qlr/ByqD+7uhHR9EyPMteZ9l7M+ybGYSCNdEtO1MiHmI6+n4pait143Q+ENedbmnHhTefpIV5hnwkDTNW6cR0ZSDf8znH7l6WbeJl599pRto6TmJE9fRLUP6qiw3gyyowezznrUcXf5dG/RaOi1rRlY0Acg0Brfom6eUOyxymfUD8U5m0kRp9R+vuRobOwqvFWBzVPc+D4O+hVdiTMzXCSJ2I3BGxCcTaz0pJQszR34zjR0CATEyBJgHfdckQpQykKRBsT8U7sto06Z0Y8ukwTDhGUx4Au9x0Xndm6mwSWMeP5ar2/wCVrh9QvcMSw+nXpmlVaHNPXkeo6Feeu+GLi5371jWzoYc4+EjSPdTY0xy1GbtMPpXTwyk8sqEgNYWue13jnBJHqvYMKsG29FtFpc7KNXOMucTuSoHCvDbLKkWghz3GXPiJ6NHgPxVyUSaTnlty5cuVIQk41CAjAQGa4i4MpXLxUY7sn/ahstd4kSIPiouFcBMp1A6o8PaPsgHU8pPRbJqMJaV9WOY0AAAQBsBsES4BLCaVpgjQW1J1+XTykq2vKuVm8mB6qFw/RhjnfxER6f8AJ9lKrCcvg4fQpwFptyNDeg/5QUqZc7tHbbNH3lEymXmT8v3qTmEwqBL2pFJx/lKDD7guptJOsb9d/qnLpktjqo1tT/dObzG3mDogLNx016b+PJRcNqb0ydtktrdB1OeYGvomR3X5gUjSqUioQen4pKpyu06ykNUE5hzCZe7VBJNV0tVddnmnn1TEKPlJKcKotalLXHwn2KrYWltaWpJ102/XmqC6pZHub0JHpy+kKacMLkSRIwrkq5BBIQEJxcgGoXJzKuQEJoRhqINTgamABqIBOBqUBAAGpYRwlDUBo7EhtNrejQff9FOmrTnWRvpGh6lKNP10VdjBMtcOSDTK10Nm+6r+0hxS0awMSEN3QPztP5qkp1O7BABOoTtCoDmhUlOrKmWteDrzCAapVYD2+WnqnadXRDduaQSBrI5eKjCp1/XsgLNlcBu6j1LlQ31R7pwAQgHad2/YfXRPMqPJ5KOzcKZQZJQEy0BhVfEFKKgd/E0e40/JXNAaqu4iOrB/V/4qapSQuhFC4hBAhJCOEhS0AQkRpIQArkULkB//2Q==" alt="Изображение товара" class="product-image">
    <p>Это описание товара. Здесь вы можете указать все детали о вашем продукте, его характеристики и преимущества.</p>
    <p class="price">Цена: 1999 ₽</p>
    <a href="https://t.me/YourBotUsername?start=buy_product" class="buy-button">Купить через Telegram</a>
</div>

</body>
</html>
