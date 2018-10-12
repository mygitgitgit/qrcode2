$qrcode = new QrReader($_FILES['file']['tmp_name']);
        $text = $qrcode->text();
        $arr=[
            'code'=>0,
            'msg'=>'',
            'data'=>['url'=>strtolower($text)]
        ];
        echo json_encode($arr);