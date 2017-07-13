# G711Decode
一个G711 PCM 音频数据互转的库

//  data  需要解析的G711 数据
//  PCM_BUFFER_SIZE 一帧数据的长度
//  out_pcm   解析后的数据
-(int)G711Decode:(NSData*)data{
    //Ret = G711a2PCM( (char *)ucInBuff, (char *)ucOutBuff, Read, 0 );
    memset(out_pcm, 0, 2 * PCM_BUFFER_SIZE);
    return G711a2PCM((char*)data.bytes, (char*)out_pcm, data.length, 0);
}



里面还包含有 PCM -> G711  的解码   使用方法类似
