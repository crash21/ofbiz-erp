#  File: ./postgres/Dockerfile
#  Summary: The PostgreSQL object-relational database system provides reliability and data integrity.
#  License: MIT License
#  Company: Blockfreight, Inc.
#  Author: Julian Smith <julian.smith@blockfreight.com>, Jerram Watters <jerram.watters@blockfreight.com>, Nick Doulgeridis <nickdoulgeridis@gmail.com>
#  Site: https://blockfreight.com
#  Support: <support@blockfreight.com>

#  Blockfreight, Inc. - OFBiz (ERP) Docker Image

#  Copyright © 2018 Blockfreight, Inc. All Rights Reserved.

#  Permission is hereby granted, free of charge, to any person obtaining
#  a copy of this software and associated documentation files (the "Software"),
#  to deal in the Software without restriction, including without limitation
#  the rights to use, copy, modify, merge, publish, distribute, sublicense,
#  and/or sell copies of the Software, and to permit persons to whom the
#  Software is furnished to do so, subject to the following conditions:

#  The above copyright notice and this permission notice shall be
#  included in all copies or substantial portions of the Software.

#  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
#  OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
#  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
#  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
#  WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
#  CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

#  =================================================================================================================================================
#  =================================================================================================================================================

#  BBBBBBBBBBBb     lll                                kkk             ffff                         iii                  hhh            ttt
#  BBBB``````BBBB   lll                                kkk            fff                           ```                  hhh            ttt
#  BBBB      BBBB   lll      oooooo        ccccccc     kkk    kkkk  fffffff  rrr  rrr    eeeee      iii     gggggg ggg   hhh  hhhhh   tttttttt
#  BBBBBBBBBBBB     lll    ooo    oooo    ccc    ccc   kkk   kkk    fffffff  rrrrrrrr eee    eeee   iii   gggg   ggggg   hhhh   hhhh  tttttttt
#  BBBBBBBBBBBBBB   lll   ooo      ooo   ccc           kkkkkkk        fff    rrrr    eeeeeeeeeeeee  iii  gggg      ggg   hhh     hhh    ttt
#  BBBB       BBB   lll   ooo      ooo   ccc           kkkk kkkk      fff    rrr     eeeeeeeeeeeee  iii   ggg      ggg   hhh     hhh    ttt
#  BBBB      BBBB   lll   oooo    oooo   cccc    ccc   kkk   kkkk     fff    rrr      eee      eee  iii    ggg    gggg   hhh     hhh    tttt    ....
#  BBBBBBBBBBBBB    lll     oooooooo       ccccccc     kkk     kkkk   fff    rrr       eeeeeeeee    iii     gggggg ggg   hhh     hhh     ttttt  ....
#                                                                                                         ggg      ggg
#    Blockfreight™ | The blockchain of global freight.                                                      ggggggggg

#  =================================================================================================================================================
#  =================================================================================================================================================

# Use an official PostgreSQL bject-relational database system release as a parent image.
FROM postgres:latest

#  Package Dockerfile is a package that defines the Blockfreight, Inc. - OFBiz (ERP) Docker Image
#  and provides some useful functions to work with the BF_TX token ecosystem.
MAINTAINER Julian Smith <julian.smith@blockfreight.com>

#  Copy PostgreSQL database initialisation script.
COPY init_dbs.sh /docker-entrypoint-initdb.d

#  Modify file execution permission to allow all (owner,group and other) to execute the initialisation script.
RUN chmod a+x /docker-entrypoint-initdb.d/init_dbs.sh 