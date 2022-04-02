# 1 数据可视化

## 1.1 绘图颜色

```
[allThemes, allColors] = getColors();
%% 所有颜色
figure;
tiledlayout(6, 10, 'TileSpacing', 'compact','Padding','Compact');
for j = 1:60
    nexttile
    demoPlot();
    set(gca, 'colororder', allThemes{j});
end

%% 指定颜色
figure;
x = 1:1:100;
y = log(x);
for i = 1:6
    plot(x, y + i, 'o-', 'Color', allThemes{2}(i,:), 'LineWidth', 2); % 指定第2个主题的第i个颜色
    hold on
end
hold off
```

<img src="MATLAB案例及使用技巧.assets/所有颜色.png" alt="所有颜色" style="zoom:50%;" />

<img src="MATLAB案例及使用技巧.assets/指定颜色.png" alt="指定颜色" style="zoom:50%;" />

### 1.1.1 函数说明

```
function [allThemes, allColors] = getColors()
%GETCOLORS 获取绘图颜色
%   allThemes: 所有主题的颜色， 每个主题包含六种颜色
%   allColors: 所有颜色， 主题数*6

    colorString{1} = {'#FD6D5A', '#FEB40B', '#6DC354', '#994487', '#518CD8', '#443295'};
    colorString{2} = {'#264653', '#2A9D8F', '#E9C46A', '#F4A261', '#E76F51', '#253777'};
    colorString{3} = {'#C1C976', '#C8A9A1', '#FEC2E4', '#77CCE0', '#FFD372', '#F88078'};
    colorString{4} = {'#104FFF', '#2FD151', '#64C7B8', '#FF1038', '#45CAFF', '#B913FF'};
    colorString{5} = {'#4C87D6', '#F38562', '#F2B825', '#D4C114', '#88B421', '#199FE0'};
    colorString{6} = {'#037CD2', '#00AAAA', '#927FD3', '#E54E5D', '#EAA700', '#F57F4B'};
    colorString{7} = {'#64B6EA', '#FB8857', '#A788EB', '#80D172', '#FC7A77', '#61D4D5'};
    colorString{8} = {'#F1787D', '#F8D889', '#69CDE0', '#5EB7F1', '#EDA462', '#F6C4E6'};
    colorString{9} = {'#8C8FD5', '#C0E5BC', '#8C8FD5', '#BDF4FC', '#C3BCE6', '#F48FB1'};
    colorString{10} = {'#B04A7A', '#171433', '#B6342E', '#DBB9DB', '#FAB4AC', '#EFB9C1'};
    colorString{11} = {'#E74745', '#FB7857', '#FBCD60', '#FEFB66', '#1AC0C6', '#FB7857'};
    colorString{12} = {'#361D32', '#543C52', '#F65A53', '#EED2CB', '#DBD873', '#F1E8E8'};
    colorString{13} = {'#454D66', '#319975', '#58B368', '#DBD873', '#FAC46C', '#F1ECB7'};
    colorString{14} = {'#112E92', '#112E92', '#48D6D2', '#81EAE6', '#F8F6BA', '#E3F5F6'};
    colorString{15} = {'#134036', '#103232', '#34C0B8', '#7A27FF', '#FFCA7B', '#F8A427'};
    colorString{16} = {'#FF0000', '#F65A53', '#34C0B8', '#7A27FF', '#FF98A4', '#D7BCE7'};
    colorString{17} = {'#F84D4D', '#FF6B42', '#5BA3EB', '#06BB9A', '#8E7EF0', '#F4B919'};
    colorString{18} = {'#406196', '#F4B414', '#77649B', '#385D77', '#576270', '#778495'};
    colorString{19} = {'#4C6CFF', '#18C1FF', '#3DEF2D', '#9818BC', '#CB1E86', '#FC564B'};
    colorString{20} = {'#0E9DFF', '#FF0000', '#800080', '#FFA500', '#ECE70B', '#979797'};
    colorString{21} = {'#313BD0', '#9A22F8', '#00F2F2', '#00B2FC', '#5EAFFA', '#81E0D7'};
    colorString{22} = {'#55EFC4', '#81ECEC', '#74B9FF', '#A29BFE', '#7F8C8D', '#C9C9C9'};
    colorString{23} = {'#FAD390', '#F8C291', '#3742FA', '#70A1FF', '#82CCDD', '#B8E994'};
    colorString{24} = {'#F8E0F1', '#DEC8CC', '#B87D9C', '#82447F', '#0B174E', '#C9C9C9'};
    colorString{25} = {'#0063C3', '#408AD2', '#3396CF', '#A0D284', '#F5CD39', '#BEBEBE'};
    colorString{26} = {'#4316F3', '#8769F7', '#FA807C', '#EFC09D', '#A5A5A5', '#C9C9C9'};
    colorString{27} = {'#104382', '#0A8CB2', '#448CE1', '#1BB5E1', '#FF6155', '#C9C9C9'};
    colorString{28} = {'#14BF96', '#1865F2', '#FFB100', '#073587', '#5F9ABC', '#BCBCBC'};
    colorString{29} = {'#16B99A', '#1F7CC1', '#1686F8', '#3EC5E0', '#93D06A', '#BABABA'};
    colorString{30} = {'#014AE0', '#1587FD', '#2DD3FB', '#FA6766', '#F8B613', '#BD55F9'};
    colorString{31} = {'#1987D7', '#5B73CD', '#1FBF79', '#3BB9C1', '#F86B0D', '#FAA900'};
    colorString{32} = {'#4071EC', '#FA3279', '#1096FA', '#35B9E4', '#2DCC97', '#A0B2BA'};
    colorString{33} = {'#007EB4', '#00A7FC', '#FFC85C', '#ED326C', '#A84269', '#BC4715'};
    colorString{34} = {'#F79F1F', '#A3CB38', '#1289A7', '#D980FA', '#FDA7DF', '#B53471'};
    colorString{35} = {'#FA983A', '#EB2F06', '#1E3799', '#3C6382', '#38ADA9', '#C9C9C9'};
    colorString{36} = {'#2ED573', '#1E90FF', '#3742FA', '#70A1FF', '#2F3542', '#C9C9C9'};
    colorString{37} = {'#FC5C65', '#FD9644', '#FED330', '#26DE81', '#079992', '#2BCBBA'};
    colorString{38} = {'#F3A683', '#F7D794', '#778BEB', '#70A1FF', '#E77F67', '#CF6A87'};
    colorString{39} = {'#F6B93B', '#E55039', '#4A69BD', '#60A3BC', '#78E08F', '#BBEA99'};
    colorString{40} = {'#00ADD7', '#00668A', '#F1C900', '#FFF1CE', '#E01706', '#C9C9C9'};
    colorString{41} = {'#D3DE9E', '#004965', '#17C0EB', '#FF7F78', '#3D3D3D', '#FFF200'};
    colorString{42} = {'#CD84F1', '#FFCCCC', '#FF4D4D', '#FFAF40', '#2F3542', '#FFFA65'};
    colorString{43} = {'#F53B57', '#3C40C6', '#3C40C6', '#00D8D6', '#05C46B', '#C9C9C9'};
    colorString{44} = {'#50514F', '#F45E58', '#FFE15B', '#1D7AA2', '#6DC1B3', '#A5B1C2'};
    colorString{45} = {'#FFC312', '#12CBC4', '#C4E538', '#1289A7', '#FDA7DF', '#ED4C67'};
    colorString{46} = {'#FFC000', '#EA3C6E', '#1B73A7', '#2C946E', '#A5B1C2', '#303952'};
    colorString{47} = {'#A589C6', '#FD91A0', '#F2E9DA', '#DFE384', '#39BFCB', '#A6E3E8'};
    colorString{48} = {'#CC99FF', '#FFAFD7', '#9BCDFF', '#FFD0A1', '#99FFCC', '#CCFF9A'};
    colorString{49} = {'#3F48CC', '#B83DBA', '#FF7F27', '#0ED145', '#EC1C24', '#A76E4E'};
    colorString{50} = {'#385261', '#7298AB', '#4F9A73', '#74878B', '#86AEA6', '#D1F0F3'};% 高级红
    colorString{51} = {'#ED5736', '#C61D34', '#F30D00', '#DD5A6C', '#F00057', '#FE0096'};% 高级蓝
    colorString{52} = {'#4B59C2', '#5A77BB', '#4A94C5', '#3B2E7E', '#013370', '#1A2946'};% 高级绿
    colorString{53} = {'#08DE9E', '#01E400', '#21A576', '#BDDD20', '#9DBC20', '#67945B'};% 高级紫
    colorString{54} = {'#7F1EAC', '#815377', '#57004F', '#4C211B', '#CBA4E5', '#A5A9D6'};% 高级深色
    colorString{55} = {'#2D445F', '#3F4D50', '#494263', '#2279B6', '#7B9067', '#B56B62'};
    colorString{56} = {'#101420', '#4C000A', '#1A5599', '#8E2961', '#407D53', '#8E2961'};
    colorString{57} = {'#0095B6', '#4FA485', '#81D8D0', '#E2AF42', '#B8CE8E', '#9AB4CD'};
    colorString{58} = {'#005EAD', '#AF6DE5', '#719FFB', '#1CAC99', '#FE9499', '#4A8FDE'};
    colorString{58} = {'#4DE890', '#2178B8', '#77A2E8', '#F86067', '#26C4B8', '#0094C5'};
    colorString{58} = {'#5AE7E4', '#2E9F79', '#3638AE', '#FF7F00', '#FA9B97', '#30A02D'};
    colorString{58} = {'#B0E188', '#2077B5', '#05B9C7', '#A8CBE4', '#F5FFB3', '#BEECAF'};
    colorString{59} = {'#FFA1C4', '#8770E0', '#01AFEE', '#4574C6', '#FDC100', '#BAD0C4'};
    colorString{60} = {'#4AB9EE', '#FF178D', '#FF178D', '#FFD600', '#00B1A1', '#97D601'};
    
    tCount = length(colorString);   % 主题数目
    cCount = sum(cellfun(@length, colorString)); % 所有的颜色数目
    allColors = nan(cCount, 3);   
    allThemes = cell(tCount, 1);
    
    idx = 1;
    for i = 1 : length(colorString)
        color = nan(length(colorString{i}), 3);
        for j = 1 : length(colorString{i})
            % 注意这里的RGB值是0-255范围
            rgb = hex2rgb(colorString{i}{j});
            allColors(idx, :) = rgb2matlabcolor(rgb);
            color(j, :) = allColors(idx, :);
            idx = idx + 1;
        end
        allThemes{i} = color;
    end

end
```

```
function [c] = hex2rgb(str)
%HEX2RGB 十六进制颜色转成RGB颜色数组
%   c: rgb颜色数组, [4, 4, 4]
%   str: 十六进制颜色, '#FD6D5A'

    clist = '0123456789ABCDEF';
    nums = zeros(1, 6);
    for i = 1:6
        nums(i) = find(str(i + 1) == clist);
    end
    c = zeros(1, 3);    % 两位十六进制数表示一个独立颜色
    for i = 1:3
        c(i) = 16 * (nums(2*i-1) - 1) + (nums(2*i) - 1);
    end
end
```

```
function [c] = rgb2matlabcolor(rgb)
%RGB2MATLABCOLOR rgb转换为matlab颜色变量
%   rgb: rgb颜色数组, [4, 4, 4]
%   c: matlab的rgb颜色
    c = round(100 * rgb/255) / 100;
end
```

```
function [] = demoPlot()
%DEMOPLOT 绘制6条曲线
%   此处显示详细说明
    x = 1:1:6;
    y = ones(1, length(x));
    for i = 1:6
        plot(x, y + i, 'LineWidth', 8);
        axis off
        hold on
    end
    hold off
end
```

##  1.2 二维绘图

### 1.2.1 渐变色

```
clear;clc;close all;
%% 获取到颜色
[allThemes, allColors] = getColors();
x = linspace(0, 3*pi, 360);
y = sin(2*x);
%% 渐变色填充
figure;
fill(x, y, y, 'EdgeColor', 'interp');
colormap("autumn");
%% 渐变色曲线
figure;
fill([x, NaN], [y, NaN], [y, NaN], 'EdgeColor', 'interp', 'LineWidth', 2);
colormap(allThemes{1});
%% 渐变色散点
figure;
scatter(x, y, [], x, 'filled');
colormap(allColors);
```

<img src="MATLAB案例及使用技巧.assets/渐变色填充.png" alt="渐变色填充" style="zoom:50%;" />

<img src="MATLAB案例及使用技巧.assets/渐变色曲线.png" alt="渐变色曲线" style="zoom: 50%;" />

<img src="MATLAB案例及使用技巧.assets/渐变色散点.png" alt="渐变色散点" style="zoom:50%;" />

## 常用代码段

### 保留和复制绘图时保留最少的空白

```
% 'TileSpacing','Compact'最小化绘图之间的空间
% 'Padding','Compact'布局周围的空间最小化
t = tiledlayout(2,2,'TileSpacing','Compact','Padding','Compact');
nexttile
plot([0 1])
nexttile
plot([1 0])
nexttile
plot([0 1 0 1])
nexttile
plot([1 0 1 0])

% 将布局另存为 PDF 文件，使用透明背景保存 PDF
exportgraphics(t,'fourplots.pdf','BackgroundColor','none')

% 将布局复制到剪贴板
copygraphics(t,'BackgroundColor','none')
```

