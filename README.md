# Others

Qt Project Settings


QT       += core gui opengl

greaterThan(QT_MAJOR_VERSION, 4): QT += widgets

TARGET = qmesher
TEMPLATE = app


SOURCES += main.cpp\
        mainwindow.cpp \
    occview.cpp \
    geometry.cpp \
    mesh.cpp

HEADERS  += mainwindow.h \
    occview.h \
    geometry.h \
    mesh.h

FORMS    += mainwindow.ui

QMAKE_CXXFLAGS += -std=c++11\
    -D_GLIBCXX_USE_CXX11_ABI=0

INCLUDEPATH +=  \
        /usr/local/include/opencascade \

LIBS +=         \
        -L /usr/local/lib \

LIBS +=         \
    -lTKernel   \
    -lTKMath    \
    -lTKG3d     \
    -lTKBRep    \
    -lTKGeomBase\
    -lTKGeomAlgo\
    -lTKTopAlgo \
    -lTKPrim    \
    -lTKBO      \
    -lTKBool    \
    -lTKOffset  \
    -lTKService \
    -lTKV3d     \
    -lTKOpenGl  \
    -lTKFillet  \
    -lTKSTEPBase \
    -lTKSTEP    \
    -lTKXSBase  \

INCLUDEPATH += /home/johnx//Downloads/gmsh-4.1.4-Linux64-sdk/include

LIBS += -L/home/johnx/Downloads/gmsh-4.1.4-Linux64-sdk/lib/ -lgmsh
