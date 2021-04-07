# An English Assignment
## 这是一个二级标题
#### 这是一个四级标题

1. 这是一个链接  
    - [百度网址](http://www.baidu.com)

2. 这是一个图片   
    ![百度图标](https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png)

3. 这是代码区  
  
    csi_trace = read_bf_file('sample_data/walk_LoS.dat');

    for i=1:200%这里是取的数据包的个数
          csi_entry = csi_trace{i};
          csi = get_scaled_csi(csi_entry); %提取csi矩阵    
          csi =csi(1,:,:);
          csi1=abs(squeeze(csi).');          %提取幅值(降维+转置)

          %只取一根天线的数据
          first_ant_csi(:,i)=csi1(:,1);           %直接取第一列数据(不需要for循环取)
          second_ant_csi(:,i)=csi1(:,2)
          third_ant_csi(:,i)=csi1(:,3)

    %     for j=1:30
    %         csi15_end(i,:)=csi1(j,:);           %3个信道第j个子载波
    %     end
    end

    %画第一根天线的载波
    %plot(first_ant_csi.')
    plot(second_ant_csi.')
    %plot(third_ant_csi.')
4. 其他
   > *斜体文本*
   > _斜体文本_
   > **粗体文本**
   > __粗体文本__
   > ***粗斜体文本***
   > ___粗斜体文本___
